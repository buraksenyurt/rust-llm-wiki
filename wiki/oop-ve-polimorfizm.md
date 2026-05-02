# OOP ve Polimorfizm

**Özet**: Bu sayfa, Rust'ta OOP benzeri yapıların struct, trait, generic ve trait object kombinasyonlarıyla nasıl kurulduğunu özetler.

**Kaynaklar**: `2022-04-24-rust-pratikleri-oop.md`, `2022-05-01-rust-pratikleri-trait-objects.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Rust'ta klasik class yapısı yoktur; buna rağmen struct, enum, impl blokları ve trait'ler ile kapsülleme, davranış ekleme ve arayüz benzeri soyutlama kurulabilir (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- Kalıtım yerine composition öne çıkar; bir yapıyı başka bir yapının alanı olarak taşımak, davranış paylaşımını daha açık ve denetlenebilir hale getirir (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- Generic trait bound'ları static dispatch üretir; bu yaklaşım derleme zamanında her somut tip için uzmanlaşmış kod oluşmasına dayanır (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- Trait object kullanımı ise `Box<dyn Trait>` gibi yapılarla farklı somut tipleri aynı koleksiyonda tutmayı ve runtime polymorphism kurmayı mümkün kılar (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).
- Plugin benzeri genişleyebilir tasarımlar, trait object kullanan heterojen koleksiyonlar sayesinde yeni tipleri mevcut yapıyı bozmadan sisteme ekleyebilir (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).

## İlgili sayfalar

- [[rust-pratikleri-oop]]
- [[rust-pratikleri-trait-objects]]
- [[state-tasarim-kalibi-ve-durum-gecisleri]]
