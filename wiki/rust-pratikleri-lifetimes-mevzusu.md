# Rust Pratikleri - Lifetimes Mevzusu

**Özet**: Bu sayfa, explicit lifetime yazımı ile `String` ve `&str` tercihinin neden önemli olduğunu özetler.

**Kaynaklar**: `2022-03-06-rust-pratikleri-lifetimes-mevzusu.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Yazı, `String` ile `&str` arasındaki ayrımı bellek maliyeti ve değiştirilebilirlik üzerinden açıklayarak başlar (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- Lifetime parametreleri, referansların geçerli kapsamını görünür hale getirip dangling pointer oluşmasını derleme zamanında engeller (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- Buffer tabanlı senaryolarda değişmeyecek metin parçalarını `&str` ile taşımak, gereksiz allocation maliyetini azaltabilir (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- Struct ve impl bloklarında explicit lifetime yazımı gerektiğinde, bu bilgi API sözleşmesinin parçası haline gelir (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).

## İlgili sayfalar

- [[lifetimes-ve-string-slice]]
- [[sahiplik-ve-borclanma]]
