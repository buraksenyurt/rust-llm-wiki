# Rust Pratikleri - OOP

**Özet**: Bu sayfa, Rust'ta OOP kavramlarının struct, trait, composition ve dispatch seçenekleri üzerinden nasıl kurulduğunu özetler.

**Kaynaklar**: `2022-04-24-rust-pratikleri-oop.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Yazı, Rust'ta class bulunmasa da struct, enum, impl blokları ve trait'lerle kapsülleme ve davranış modellemenin kurulabildiğini gösterir (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- Kalıtım yerine composition tercih edilir; veri ve davranış paylaşımı alanlar ve trait implementasyonları üzerinden daha açık yürütülür (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- Generic trait bound kullanımı static dispatch üretirken, polimorfik davranış trait tabanlı arayüzlerle kurulabilir (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- Enum varyantlarının veri taşıyabilmesi, geleneksel OOP modeline ek olarak daha zengin durum modelleme seçenekleri sunar (kaynak: 2022-04-24-rust-pratikleri-oop.md).

## İlgili sayfalar

- [[oop-ve-polimorfizm]]
- [[enum-ile-durum-modelleme]]
