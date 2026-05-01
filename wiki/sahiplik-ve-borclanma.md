# Sahiplik ve Borçlanma

**Özet**: Bu sayfa, Rust'ın sahiplik ve borçlanma modelinin bellek güvenliği, API tasarımı ve performans üzerindeki etkisini toplu biçimde özetler.

**Kaynaklar**: `2025-02-14-rust-ve-guvenli-bellek-yonetimi-hakkinda.md`, `2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md`, `2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md`, `2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md`

**Son güncelleme**: 2026-05-01

---

## Temel noktalar

- Rust'ta bir değerin sahipliği belirli bir anda tek bir yerde tutulur; bu ilke, bellek güvenliğinin omurgası olarak ownership ve borrow checker ile birlikte anlatılır (kaynak: 2025-02-14-rust-ve-guvenli-bellek-yonetimi-hakkinda.md).
- Bir değeri başka fonksiyona taşımak, orijinal değişkenin artık kullanılamaması sonucunu doğurabilir; 2026-01-15 tarihli karşılaştırma yazısı bunu metot argümanları üzerinden açık örnekle gösterir (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Değiştirilebilir erişim niyeti Rust'ta açıkça `&mut` ile belirtilir; yalnızca değişkeni `mut` tanımlamak bu niyetin başka fonksiyona otomatik taşındığı anlamına gelmez (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Başlangıç seviyesi pratikler yazısı, gereksiz `clone` çağrılarını azaltmak için referans ve slice kullanımını; sahipliği korumak gerektiğinde veri yerine referans aktarmayı önerir (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- Çoklu thread senaryolarında sahiplik ilkesi ortadan kalkmaz; yalnızca Arc gibi araçlarla çoklu sahiplik açık biçimde modellenir ve mutasyon gerekiyorsa bu, Mutex gibi ek bir katmanla güvenli hale getirilir (kaynak: 2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md).

## İlgili sayfalar

- [[bellek-guvenligi]]
- [[enum-ile-durum-modelleme]]
- [[eszamanlilik-ve-paylasilan-durum]]
