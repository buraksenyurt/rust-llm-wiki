# Rust ile Kodlama İdmanları - Başlangıç Seviyesi

**Özet**: Bu sayfa, Rust öğrenirken erken dönemde edinilmesi gereken temel kodlama alışkanlıklarını kısa başlıklar halinde toparlar.

**Kaynaklar**: `2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md`

**Son güncelleme**: 2026-05-01

---

## Temel noktalar

- Makale, üretim kodunda `unwrap` ve `expect` kullanımından kaçınmayı; bunun yerine `Option` ve `Result` akışlarını açık biçimde ele almayı önerir (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- Gereksiz `clone` çağrılarını azaltmak için koleksiyon ve dizgilerin referans veya slice üzerinden taşınması tavsiye edilir (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- Mutasyon kapsamını dar tutmak ve varsayılanı immutable bırakmak, makaledeki iyi pratiklerden biridir (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- Dangling referanslardan kaçınma, sahipliği gerektiğinde devretme ve ömürleri doğru kurgulama, başlangıç seviyesinde kritik başlıklar arasında sayılır (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- Public API'lerde markdown tabanlı kapsamlı dokümantasyon kullanımının önemli olduğu özellikle vurgulanır (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- Makale ayrıca sahipliği göz ardı etmek için uygun referans geçişlerini, makroları dikkatli kullanmayı, `String` yerine uygun yerde `&str` tercih etmeyi ve tek varyantlı eşleşmelerde `if let` kullanımını örnekler (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[bellek-guvenligi]]
- [[rust-ile-kodlama-idmanlari-orta-seviye]]
