# Rust Pratikleri - Dokümantasyon

**Özet**: Bu sayfa, Rust kodlarında dökümantasyon yorumları yazma, HTML çıktı üretme ve örnekleri test etme akışını özetler.

**Kaynaklar**: `2022-02-13-rust-pratikleri-dokumantasyon.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- `///` ve `//!` yorumları ile modül, struct ve fonksiyon düzeyinde Markdown tabanlı dokümantasyon yazılabilir (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- `cargo doc` komutu HTML belgeleri üretir; `--no-deps` ile yalnızca proje odaklı bir çıktı almak mümkündür (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- Dökümantasyon içine gömülü örneklerin `cargo test --doc` ile çalıştırılabilmesi, açıklama ile gerçek kodun senkron kalmasına yardımcı olur (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- Yazı ayrıca `cargo clippy` ile idiomatik önerilerin geliştirme deneyimini beslediğini hatırlatır (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).

## İlgili sayfalar

- [[dokumantasyon-ve-cargo-doc]]
- [[rust-pratikleri-loglama]]
