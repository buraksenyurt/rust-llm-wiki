# Rust Dilinde Phantom Type Kullanımı: PhantomData

**Özet**: `PhantomData<T>` yapısının ne olduğunu, neden gerektiğini ve nasıl kullanıldığını; Zero-Sized Types (ZST), derleme zamanı tür güvenliği, unsafe kod alanlarında drop check ve variance kalıpları üzerinden açıklayan kaynak özeti.

**Kaynaklar**: `2026-05-09-rust-phantom-data.md`

**Son güncelleme**: 2026-05-09

---

## Temel kavramlar

- **PhantomData\<T\>**: Çalışma zamanında **0 byte** yer kaplayan ancak derleyiciye tür bilgisi veren `std::marker` yapısı. Ownership, borrowing ve lifetime kurallarını etkiler; bu yüzden "hayalet" olarak adlandırılır. (kaynak: 2026-05-09-rust-phantom-data.md)
- **Zero-Sized Types (ZST)**: Herhangi bir alan içermeyen struct'lar. Rust derleyicisi bu türler için bellek tahsisi yapmaz; boyutları sıfırdır. `PhantomData` da bir ZST'dir. (kaynak: 2026-05-09-rust-phantom-data.md)

## Derleme zamanı tür güvenliği

Generic bir yapıya `PhantomData<T>` eklenerek tür etiketi (type tag) işlevi görülür. Örneğin `Component<Html>` ile `Component<MobileIos>` birbirinin yerine geçemez; yanlış türde bileşen kullanılmaya çalışıldığında derleyici `mismatched types` hatası üretir. Çalışma zamanında ise tür bilgisi saklanmadığından herhangi bir performans maliyeti oluşmaz; vtable veya dynamic dispatch söz konusu değildir. (kaynak: 2026-05-09-rust-phantom-data.md)

## Unsafe kod ve drop check

`*const T` / `*mut T` gibi raw pointer'lar sahiplik bilgisi taşımaz. Kendi bellek yönetimini yapan container'lar inşa edilirken `PhantomData<T>` eklenerek derleyiciye *"Bu yapı T'ye sahiptir; drop gerçekleştiğinde T de drop edilmelidir"* garantisi verilir. Bu sayede drop check mekanizması doğru çalışır ve dangling pointer riski ortadan kalkar. (kaynak: 2026-05-09-rust-phantom-data.md)

## Variance kalıpları

| **Kalıp** | **Anlamı** |
| --- | --- |
| `PhantomData<T>` | T'nin sahibiymişim gibi davran (covariant). |
| `PhantomData<&'a T>` | `'a` boyunca geçerli T referansına bağlıyım. |
| `PhantomData<&'a mut T>` | `'a` boyunca mutable T erişimine bağlıyım. |
| `PhantomData<*const T>` | T'ye raw const pointer gibi bağlıyım; sahip değilim. |
| `PhantomData<*mut T>` | T'ye raw mutable pointer gibi bağlıyım; invariant. |
| `PhantomData<fn(T)>` | T input pozisyonunda; contravariant. |
| `PhantomData<fn() -> T>` | T output pozisyonunda; covariant. |
| `PhantomData<fn(T) -> T>` | T hem input hem output; invariant. |
| `PhantomData<Cell<&'a ()>>` | Interior mutability; invariant lifetime etkisi. |

(kaynak: 2026-05-09-rust-phantom-data.md)

## Trait ile karşılaştırma

> Trait'ler **"What you can do with a type"** sorusuna cevap verirken, PhantomData **"What kind of thing it is"** sorusuna cevap verir.

Trait'ler çalışma zamanında da rol oynar ve dynamic dispatch maliyeti getirebilir. Eğer tür bilgisi yalnızca derleme zamanında kullanılacaksa `PhantomData` daha verimlidir. (kaynak: 2026-05-09-rust-phantom-data.md)

---

## İlgili sayfalar

- [[phantom-data]]
- [[bellek-guvenligi]]
- [[sahiplik-ve-borclanma]]
- [[lifetimes-ve-string-slice]]
- [[bellek-optimizasyonu]]
- [[oop-ve-polimorfizm]]
- [[rust-pratikleri-trait-objects]]
