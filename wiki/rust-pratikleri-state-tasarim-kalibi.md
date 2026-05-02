# Rust Pratikleri - State Tasarım Kalıbı

**Özet**: Bu sayfa, Rust'ta state pattern ile durum geçişlerini trait object ve kontrollü API üzerinden yönetme yaklaşımını özetler.

**Kaynaklar**: `2022-05-15-rust-pratikleri-state-tasarim-kalibi.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Yazı, bir değişiklik isteğinin Draft, WaitingForApproval ve Committed gibi durumlar arasında güvenli geçişini örnekler (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- Her state, aynı trait'in farklı implementasyonuyla davranışını tanımlar; geçersiz geçişler etkisiz bırakılarak akış denetlenir (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- Aktif state'in `Option<Box<dyn State>>` ile tutulması, hem tek sahiplik hem de runtime polymorphism ihtiyacını aynı yerde karşılar (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- Unit testler, geçiş sırasının doğru kaldığını ve bilgi görünürlüğünün state'e göre değiştiğini doğrular (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).

## İlgili sayfalar

- [[state-tasarim-kalibi-ve-durum-gecisleri]]
- [[enum-ile-durum-modelleme]]
- [[oop-ve-polimorfizm]]
