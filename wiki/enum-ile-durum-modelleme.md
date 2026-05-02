# Enum ile Durum Modelleme

**Özet**: Bu sayfa, Rust'ta enum ve durum geçişi odaklı tasarımların geçersiz kombinasyonları azaltmak için nasıl kullanıldığını özetler.

**Kaynaklar**: `2022-05-15-rust-pratikleri-state-tasarim-kalibi.md`, `2025-02-12-enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi.md`, `2025-12-01-rust-ile-kodlama-idmanlari-ileri-seviye.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- 2025-02-12 tarihli yazı, enum varyantlarının kendi alanlarını taşıyabilmesi sayesinde durumun veri modeli içinde doğrudan temsil edilebildiğini ve geçersiz kombinasyonların azaltılabildiğini gösterir (kaynak: 2025-02-12-enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi.md).
- Pattern matching, enum ile durum modellemenin doğal tamamlayıcısıdır; çünkü tüketen kodun bütün olası durumları görmesini zorlar (kaynak: 2025-02-12-enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi.md).
- 2022-05-15 tarihli state pattern yazısı, benzer problemi trait object ve kontrollü geçiş fonksiyonlarıyla çözer; böylece enum tabanlı modelleme ile nesne davranışına dayalı durum yönetimi arasında pratik bir köprü kurar (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- İleri seviye idmanlardaki typestate yaklaşımı, hangi işlemin hangi durumda geçerli olduğunu tür sistemiyle daha katı biçimde garanti altına alma fikrini sürdürür (kaynak: 2025-12-01-rust-ile-kodlama-idmanlari-ileri-seviye.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[state-tasarim-kalibi-ve-durum-gecisleri]]
- [[enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi]]
