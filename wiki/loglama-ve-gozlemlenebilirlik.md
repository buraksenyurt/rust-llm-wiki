# Loglama ve Gözlemlenebilirlik

**Özet**: Bu sayfa, Rust uygulamalarında log seviyeleri, facade yaklaşımı ve ortam değişkeni tabanlı yapılandırmayı özetler.

**Kaynaklar**: `2022-01-30-rust-pratikleri-loglama.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Rust ekosisteminde `log` paketi ortak facade görevi görür; `env_logger`, `log4rs` ve benzeri uygulamalar bu arayüzü kullanarak farklı hedeflere log yazabilir (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- Temel log seviyeleri `trace`, `debug`, `info`, `warn` ve `error` olarak ayrılır; uygulamanın çalışırken ne kadar ayrıntı üreteceği bu seviyelerle kontrol edilir (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- `env_logger::init()` çağrısı ve `RUST_LOG` ortam değişkeni, terminal odaklı uygulamalarda hızlı bir loglama kurulumu sağlar (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- Log target kullanımı, mesajları modül veya alt sistem bazında ayırarak aynı uygulama içinde daha okunabilir gözlemlenebilirlik sağlar (kaynak: 2022-01-30-rust-pratikleri-loglama.md).

## İlgili sayfalar

- [[rust-pratikleri-loglama]]
- [[dokumantasyon-ve-cargo-doc]]
