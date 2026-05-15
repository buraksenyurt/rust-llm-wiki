# PhantomData ve Zero-Sized Types

**Özet**: Rust'ta `PhantomData<T>` kullanarak çalışma zamanı maliyeti olmadan derleme zamanında tür güvenliği, ownership semantiği ve drop check garantisi sağlama.

**Kaynaklar**: `2026-05-09-rust-phantom-data.md`

**Son güncelleme**: 2026-05-09

---

## Ne zaman kullanılır?

`PhantomData` aşağıdaki senaryolarda tercih edilir:

- **Derleme zamanı etiketleme**: Aynı generic yapının farklı türlere özel davranmasını sağlamak. (örn. `Identity<FirstPersonShooter>` ile `Identity<RolePlayingGame>` birbirine atanamamalı) (kaynak: 2026-05-09-rust-phantom-data.md)
- **Unsafe container'lar**: Raw pointer içeren `Box`, `Vec` benzeri özel veri yapılarında drop check'i doğru yönlendirmek. (kaynak: 2026-05-09-rust-phantom-data.md)
- **FFI sarmalayıcılar**: C veya başka dillerden gelen pointer'ları Rust tür sistemiyle güvenli biçimde sarmak. (kaynak: 2026-05-09-rust-phantom-data.md)
- **Iterator ve buffer tasarımı**: Rust standart kütüphanesindeki `Iter<'a, T>` gibi yapılarda `PhantomData<&'a T>` ile lifetime bağı kurmak. (kaynak: 2026-05-09-rust-phantom-data.md)

## Temel özellikler

- Boyutu sıfırdır → çalışma zamanında bellek tahsisi yapılmaz. (kaynak: 2026-05-09-rust-phantom-data.md)
- `std::marker::PhantomData` ile içe aktarılır. (kaynak: 2026-05-09-rust-phantom-data.md)
- Derleyiciye ownership / borrowing / lifetime bilgisi taşır; runtime'da hiçbir etkisi yoktur. (kaynak: 2026-05-09-rust-phantom-data.md)
- Trait'lerden farklı olarak dynamic dispatch veya vtable maliyeti getirmez. (kaynak: 2026-05-09-rust-phantom-data.md)

## Örnek: Tür güvenli bileşen

```rust
use std::marker::PhantomData;

struct Html;
struct MobileIos;

struct Component<Render> {
    content: String,
    marker: PhantomData<Render>,
}

fn render_button(button: &Component<Html>) { /* ... */ }

// render_button(&ios_component); // derleme hatası: mismatched types
```

## Örnek: Drop check ile unsafe container

```rust
use std::marker::PhantomData;

struct SomeBox<T> {
    p: *mut T,
    _marker: PhantomData<T>, // Derleyiciye: SomeBox<T>, T'ye sahiptir
}

impl<T> Drop for SomeBox<T> {
    fn drop(&mut self) {
        unsafe { let _ = Box::from_raw(self.p); }
    }
}
```

`PhantomData<T>` olmadan derleyici `T`'nin ne zaman drop edileceğini bilemez; dangling pointer riski doğabilir. (kaynak: 2026-05-09-rust-phantom-data.md)

---

## İlgili sayfalar

- [[rust-phantom-data]]
- [[bellek-guvenligi]]
- [[sahiplik-ve-borclanma]]
- [[lifetimes-ve-string-slice]]
- [[bellek-optimizasyonu]]
- [[oop-ve-polimorfizm]]
- [[rust-pratikleri-trait-objects]]
