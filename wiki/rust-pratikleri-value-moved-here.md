# Rust Pratikleri - Value Moved Here

**Özet**: Bu sayfa, Rust'ta move semantiği, stack-heap ilişkisi ve sahipliği geri kazanma seçeneklerini özetler.

**Kaynaklar**: `2022-05-22-rust-pratikleri-value-moved-here.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Yazı, bir değerin aynı anda tek sahibi olabileceğini ve atama ile fonksiyon çağrılarının çoğu zaman sahiplik taşıdığı gerçeğini temel örneklerle gösterir (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).
- `String` gibi heap tabanlı tipler move davranışı gösterirken, `i32` gibi `Copy` trait'li tipler kopyalanarak aktarılabilir (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).
- Fonksiyona taşınan sahipliği geri almak için değeri dönüş değeri olarak yeniden döndürmek mümkündür; bu, geçici sahiplik transferini açık hale getirir (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).
- Stack frame ve drop davranışı üzerinden anlatılan örnekler, ownership'in bellek temizliğiyle doğrudan ilişkisini görünür kılar (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[gdb-ile-debugging]]
- [[programcidan-programciya-rust]]
- [[rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak]]
