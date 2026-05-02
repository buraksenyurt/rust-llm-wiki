# Terminal Uygulamaları ve Oyun Döngüsü

**Özet**: Bu sayfa, Rust'ta terminal tabanlı küçük uygulamalar kurarken metin işleme, oyun döngüsü ve kullanıcı girdisi yönetimini özetler.

**Kaynaklar**: `2022-03-13-rust-pratikleri-serde-json-ve-biraz-eglence.md`, `2022-04-10-rust-pratikleri-wordle-oyunu.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- Terminal tabanlı uygulamalarda `std::env::args` ile komut satırı argümanları alınabilir; `match` ve iterator akışları ile davranış farklı komutlara göre ayrıştırılabilir (kaynak: 2022-03-13-rust-pratikleri-serde-json-ve-biraz-eglence.md).
- `include_str!` makrosu, kelime listesi gibi sabit dosyaları derleme zamanında gömerek dağıtımı kolaylaştırır ve dosya erişim ihtiyacını azaltır (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- HashSet ile daha önce denenmiş harfleri saklamak, renkli çıktı için `colored` kullanmak ve rastgele seçim yapmak, küçük oyun döngülerinin ergonomisini artırır (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- Unit testler, terminal uygulamalarında bile iş kurallarını ayırıp doğrulamayı mümkün kılar; Wordle örneği bunu oyun durumları üzerinden gösterir (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).

## İlgili sayfalar

- [[serde-ve-json]]
- [[rust-pratikleri-wordle-oyunu]]
- [[rust-pratikleri-serde-json-ve-biraz-eglence]]
