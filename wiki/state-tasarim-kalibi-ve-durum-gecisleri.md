# State Tasarım Kalıbı ve Durum Geçişleri

**Özet**: Bu sayfa, Rust'ta durum geçişlerini kontrollü hale getirmek için kullanılan state pattern yaklaşımını özetler.

**Kaynaklar**: `2022-05-15-rust-pratikleri-state-tasarim-kalibi.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- State pattern, bir nesnenin geçebileceği durumları ve bu durumlar arasındaki hareketi açık fonksiyonlarla sınırlandırmak için kullanılır; örnek akış Draft, WaitingForApproval ve Committed adımlarını içerir (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- Her state kendi davranışını trait implementasyonu içinde tanımlar; geçersiz geçişler doğrudan reddedilmese de aynı state'i geri döndürerek etkisiz bırakılabilir (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- `Option<Box<dyn State>>` kullanımı, aktif durumu tek sahipli bir trait object olarak saklamayı ve geçiş sırasında sahipliği kontrollü biçimde devretmeyi sağlar (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- Unit testler, bilgi ekleme ve onaylama gibi akışların beklenen sırada işlendiğini doğrulayarak pattern'in davranışını görünür kılar (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).

## İlgili sayfalar

- [[enum-ile-durum-modelleme]]
- [[oop-ve-polimorfizm]]
- [[rust-pratikleri-state-tasarim-kalibi]]
