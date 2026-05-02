# Lifetimes ve String Slice

**Özet**: Bu sayfa, Rust'ta referans ömrü bildirimi ile `String` ve `&str` arasındaki seçimlerin güvenlik ve performans tarafını özetler.

**Kaynaklar**: `2021-12-24-programcidan-programciya-rust.md`, `2022-03-06-rust-pratikleri-lifetimes-mevzusu.md`, `2022-03-20-rust-pratikleri-http-sunucusu-yazmak-yazmaya-calismak.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- `String`, heap üzerinde büyüyebilen sahipli bir veri türüdür; `&str` ise çoğu durumda mevcut veriye işaret eden, daha hafif ve immutable bir slice yaklaşımı sunar (kaynak: 2021-12-24-programcidan-programciya-rust.md) (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- Lifetime parametreleri, referansların hangi kapsam boyunca geçerli olduğunu görünür hale getirerek dangling pointer üretimini derleme aşamasında engeller (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- Ağ ve buffer tabanlı senaryolarda, değişmeyecek veriyi `String` yerine `&str` ile taşımak fazladan allocation azaltabileceği için özellikle anlamlıdır (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md) (kaynak: 2022-03-20-rust-pratikleri-http-sunucusu-yazmak-yazmaya-calismak.md).
- Daha karmaşık struct ve impl bloklarında explicit lifetime yazımı gerekebilir; bu, referans bağımlılığını API seviyesinde görünür kılar (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[rust-pratikleri-lifetimes-mevzusu]]
- [[tcp-ve-http-sunucusu]]
