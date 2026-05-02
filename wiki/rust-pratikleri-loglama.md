# Rust Pratikleri - Loglama

**Özet**: Bu sayfa, Rust uygulamalarında `log` facade'i ve `env_logger` ile terminal odaklı loglama kurulumunu özetler.

**Kaynaklar**: `2022-01-30-rust-pratikleri-loglama.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Kaynak, loglamayı hata ayıklama ve akış görünürlüğü için temel ihtiyaç olarak çerçeveler; Rust ekosisteminde bu amaçla `log` facade yaklaşımını öne çıkarır (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- `env_logger::init()` ile çalışma zamanı hazırlığı yapılır ve `trace`, `debug`, `info`, `warn`, `error` seviyeleri makrolarla kullanılabilir (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- `RUST_LOG` ortam değişkeni, hangi seviye ve hedefte log üretileceğini kod değiştirmeden ayarlamaya imkân verir (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- Log target kullanımı, mesajların hangi modül veya alt sistemden geldiğini ayrıştırmayı kolaylaştırır (kaynak: 2022-01-30-rust-pratikleri-loglama.md).

## İlgili sayfalar

- [[loglama-ve-gozlemlenebilirlik]]
- [[dokumantasyon-ve-cargo-doc]]
