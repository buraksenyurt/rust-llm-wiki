# Rust Pratikleri - Değişkenleri Kopyalayarak veya Referans Olarak Taşımak

**Özet**: Bu sayfa, Copy ve Clone kullanımı ile referans geçirme tercihlerinin move davranışını nasıl etkilediğini özetler.

**Kaynaklar**: `2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Yazı, "value moved here" hatasının tipik sebebini bir değerin sahipliğinin fonksiyona veya başka değişkene taşınması üzerinden açıklar (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md).
- `Clone` ve `Copy` trait'leri, bazı türlerin kopyalanarak aktarılmasına izin vererek move sonrası kullanılamama durumunu kontrollü biçimde hafifletebilir (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md).
- Referansla geçirme yaklaşımı, sahipliği korurken fonksiyonların veriye erişmesini sağlayan daha hafif bir alternatif olarak sunulur (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md).
- GDB kullanımıyla stack frame ve argüman gözlemi yapılarak bu farklar çalışma anında görünür hale getirilir (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[gdb-ile-debugging]]
