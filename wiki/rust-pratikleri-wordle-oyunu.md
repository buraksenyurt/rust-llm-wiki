# Rust Pratikleri - Wordle Oyunu

**Özet**: Bu sayfa, terminal tabanlı bir Wordle klonunda oyun durumu, metin işleme ve testlerin nasıl bir araya geldiğini özetler.

**Kaynaklar**: `2022-04-10-rust-pratikleri-wordle-oyunu.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Kelime listesi `include_str!` ile derleme zamanında programa gömülür; bu sayede oyun harici dosya erişimine daha az ihtiyaç duyar (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- Oyun durumu bir yönetici yapı içinde tutulur; tahmin edilen harfler `HashSet` ile izlenir ve kullanıcıya renkli geri bildirim verilmek için `colored` kullanılır (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- Rastgele kelime seçimi ve iterator tabanlı metin temizleme akışı, küçük terminal oyunlarında veri hazırlama işini sadeleştirir (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- Unit testler, kelime kontrolü ve durum geçişleri gibi iş kurallarını oyun döngüsünden ayrı doğrulamayı mümkün kılar (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).

## İlgili sayfalar

- [[terminal-uygulamalari-ve-oyun-dongusu]]
- [[enum-ile-durum-modelleme]]
