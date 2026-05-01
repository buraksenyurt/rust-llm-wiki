# Bunu Bir Dene 00 - Metot Argümanlarında Değişiklik (C#, Rust ve Zig)

**Özet**: Bu sayfa, metot argümanlarında durum değiştirme davranışının C#, Rust ve Zig tarafında nasıl farklılaştığını karşılaştırmalı bir örnekle özetler.

**Kaynaklar**: `2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md`

**Son güncelleme**: 2026-05-01

---

## Temel noktalar

- Makale, C# tarafında sınıf nesnelerinin metotlara varsayılan olarak referans türü gibi iletilmesi nedeniyle içeride yapılan değişikliğin çağıranı etkileyebildiğini örnekler (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Rust örneğinde yalnızca değişkeni `mut` yapmak yeterli görülmez; değiştirilebilir borç verme niyeti `&mut` ile açık biçimde ifade edilir (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Metin, Rust'ta sahipliğin başka fonksiyona taşınması halinde orijinal değişkenin artık kullanılamayacağını ve bunun dilin tasarımının doğal sonucu olduğunu vurgular (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Zig bölümünde, fonksiyon parametrelerinin varsayılan olarak immutable kabul edildiği ve bu yüzden değişiklik için pointer üzerinden adres geçilmesi gerektiği anlatılır (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- Yazının son kısmında, ideal yaklaşım olarak durum değişikliğinin veri yapısının kendi metotları içine alınması ya da gerektiğinde yeni bir nesne örneği döndürülmesi önerilir (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[csharp-rust-zig-karsilastirmalari]]
- [[bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig]]
