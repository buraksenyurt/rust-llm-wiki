# GDB ile Debugging

**Özet**: Bu sayfa, GDB kullanarak Rust programlarında stack, heap ve pointer davranışını gözlemlemeye yönelik temel pratikleri özetler.

**Kaynaklar**: `2022-02-27-rust-pratikleri-gdb-ile-debug-islemleri.md`, `2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md`

**Son güncelleme**: 2026-05-02

---

## Temel noktalar

- GDB, Rust programlarında stack ve heap üzerindeki değerleri gözleyerek ownership ve smart pointer davranışını somutlaştırmak için yararlı bir araç olarak kullanılır (kaynak: 2022-02-27-rust-pratikleri-gdb-ile-debug-islemleri.md).
- `b`, `n`, `c`, `info locals`, `info args`, `bt` ve `print *p` gibi komutlar, hem akış kontrolünü hem de pointer içeriğini incelemek için öne çıkar (kaynak: 2022-02-27-rust-pratikleri-gdb-ile-debug-islemleri.md).
- Box ve benzeri pointer'ların scope sonundaki temizlenmesi, GDB üzerinden adres ve içerik inceleyerek daha görünür hale getirilebilir (kaynak: 2022-02-27-rust-pratikleri-gdb-ile-debug-islemleri.md).
- Copy, Clone ve referansla geçirme farkları da GDB ile stack frame ve argüman incelemesi üzerinden takip edilebilir; bu yaklaşım 2022-04-17 tarihli yazıda move kaynaklı hata mesajlarını anlamaya yardımcı olur (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md).

## İlgili sayfalar

- [[sahiplik-ve-borclanma]]
- [[rust-pratikleri-gdb-ile-debug-islemleri]]
- [[rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak]]
