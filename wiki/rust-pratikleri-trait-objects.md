# Rust Pratikleri - Trait Objects

**Özet**: Bu sayfa, `dyn Trait` kullanarak farklı somut tipleri aynı koleksiyonda toplama ve runtime polymorphism kurma yaklaşımını özetler.

**Kaynaklar**: `2022-05-01-rust-pratikleri-trait-objects.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Trait object yaklaşımı, generic'lerin tek somut tip kısıtını aşarak çalışma zamanında birden çok türü aynı sözleşme altında işletebilme imkânı verir (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).
- `Vec<Box<dyn Draw>>` benzeri koleksiyonlar, heterojen bileşenleri aynı belge ya da arayüz içinde saklamak için pratik bir desendir (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).
- `Box`, `&`, `Arc` ve `Rc` gibi taşıyıcılar trait object'leri farklı sahiplik modelleriyle kullanmaya olanak tanır (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).
- Bu yapı, plugin benzeri genişleyebilir tasarımlarda yeni bileşenleri çekirdek akışa dokunmadan eklemeyi kolaylaştırır (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).

## İlgili sayfalar

- [[oop-ve-polimorfizm]]
- [[state-tasarim-kalibi-ve-durum-gecisleri]]
