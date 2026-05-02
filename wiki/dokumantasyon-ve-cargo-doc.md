# Dokümantasyon ve Cargo Doc

**Özet**: Bu sayfa, Rust kodlarında dökümantasyon yorumları, otomatik HTML çıktısı ve doküman içi örneklerin test edilmesini özetler.

**Kaynaklar**: `2022-02-13-rust-pratikleri-dokumantasyon.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Rust'ta dış dokümantasyon yorumları `///`, iç dokümantasyon yorumları ise `//!` ile yazılır ve Markdown içeriği doğrudan desteklenir (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- `cargo doc` ile proje için HTML dokümantasyon üretilir; `--no-deps` seçeneği bağımlılıkların dökümanını hariç tutarak daha odaklı çıktı sağlar (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- Dokümantasyon içine gömülen örnek kodlar `cargo test --doc` ile çalıştırılabildiği için örneklerin yalnızca açıklayıcı değil, doğrulanabilir olması beklenir (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- Aynı yazı, `cargo clippy` uyarılarının idiomatik Rust yazımını desteklediğini ve dokümantasyonla birlikte geliştirici deneyimini güçlendirdiğini vurgular (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).

## İlgili sayfalar

- [[rust-pratikleri-dokumantasyon]]
- [[loglama-ve-gozlemlenebilirlik]]
