# Sahiplik ve Borçlanma

**Özet**: Bu sayfa, Rust'ta sahiplik, borçlanma, move semantiği ve yaşam süresi kurallarının nasıl birlikte çalıştığını toplu biçimde özetler.

**Kaynaklar**: `2021-12-24-programcidan-programciya-rust.md`, `2022-03-06-rust-pratikleri-lifetimes-mevzusu.md`, `2022-04-03-rust-pratikleri-ayni-anda-sadece-tek-bir-degistirilebilir-referans-olabilir.md`, `2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md`, `2022-05-22-rust-pratikleri-value-moved-here.md`, `2025-02-14-rust-ve-guvenli-bellek-yonetimi-hakkinda.md`, `2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md`, `2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md`, `2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Rust'ta bir değerin sahibi aynı anda tektir; bu ilke, borrow checker ve scope sonu temizliğiyle birlikte bellek güvenliğinin omurgasını oluşturur (kaynak: 2021-12-24-programcidan-programciya-rust.md) (kaynak: 2025-02-14-rust-ve-guvenli-bellek-yonetimi-hakkinda.md).
- Move semantiği nedeniyle `String` gibi heap tabanlı değerler atama veya fonksiyon çağrısı ile taşınabilir; gerekirse sahipliği geri döndürmek, referans geçirmek ya da uygun yerde `Clone` ve `Copy` kullanmak gerekir (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md) (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).
- Değiştirilebilir erişim niyeti Rust'ta açıkça `&mut` ile ifade edilir; bir değişkeni `mut` tanımlamak tek başına başka fonksiyonların onu değiştirebileceği anlamına gelmez (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Lifetime kuralları, referansların geçerli yaşam aralığını görünür hale getirerek dangling pointer oluşmasını engeller; bu yüzden `String` ile `&str` seçimi hem güvenlik hem performans konusudur (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- "Aynı anda tek bir değiştirilebilir referans" kuralı yalnızca tek thread için değil, çoklu thread akışında da etkilidir; paylaşım gerektiğinde Arc ile çoklu sahiplik, Mutex ile kontrollü mutasyon tercih edilir (kaynak: 2022-04-03-rust-pratikleri-ayni-anda-sadece-tek-bir-degistirilebilir-referans-olabilir.md) (kaynak: 2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md).
- Başlangıç seviyesi pratikler, gereksiz `clone` çağrılarını azaltmak için slice ve referans kullanımını; veri sahipliğini korumak gerektiğinde mümkün olduğunca kopya yerine ödünç verme yaklaşımını önerir (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).

## İlgili sayfalar

- [[programcidan-programciya-rust]]
- [[bellek-guvenligi]]
- [[lifetimes-ve-string-slice]]
- [[eszamanlilik-ve-paylasilan-durum]]
- [[gdb-ile-debugging]]
- [[rust-pratikleri-value-moved-here]]
- [[rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak]]
- [[bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig]]
