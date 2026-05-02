# Rust LLM Wiki

> 2026-05-02 orphan bağlantı denetimi sonrası kaynak özetleri ile kavram sayfaları arasındaki çapraz bağlar güçlendirildi.

## Kavram sayfaları

- [[sahiplik-ve-borclanma]] — Ownership, borrowing, move ve açık mutasyon niyetinin toplu özeti (kaynak: 2021-12-24-programcidan-programciya-rust.md) (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).
- [[lifetimes-ve-string-slice]] — `String` ve `&str` seçimi ile explicit lifetime kullanımının özeti (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- [[bellek-guvenligi]] — Use After Free, Double Free, Dangling Pointer ve Buffer Overflow çerçevesi (kaynak: 2025-02-14-rust-ve-guvenli-bellek-yonetimi-hakkinda.md).
- [[eszamanlilik-ve-paylasilan-durum]] — Thread oluşturma, Arc/Mutex, atomikler ve paylaşılmış mutasyon tercihleri (kaynak: 2022-04-03-rust-pratikleri-ayni-anda-sadece-tek-bir-degistirilebilir-referans-olabilir.md) (kaynak: 2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md).
- [[kanallar-ve-thread-haberlesmesi]] — FIFO kanal mantığı, MPSC ve bounded/unbounded seçimleri (kaynak: 2022-02-20-rust-pratikleri-channels.md).
- [[gdb-ile-debugging]] — GDB ile stack, heap ve pointer davranışını gözleme notları (kaynak: 2022-02-27-rust-pratikleri-gdb-ile-debug-islemleri.md).
- [[loglama-ve-gozlemlenebilirlik]] — `log` facade'i, `env_logger` ve `RUST_LOG` yapılandırması (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- [[dokumantasyon-ve-cargo-doc]] — Dokümantasyon yorumları, `cargo doc` ve doctest akışı (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- [[serde-ve-json]] — Serde ile JSON verisini Rust struct'larına dönüştürme yaklaşımı (kaynak: 2022-03-13-rust-pratikleri-serde-json-ve-biraz-eglence.md).
- [[tcp-ve-http-sunucusu]] — TCP dinleme, request parsing ve response üretme akışı (kaynak: 2022-03-20-rust-pratikleri-http-sunucusu-yazmak-yazmaya-calismak.md).
- [[terminal-uygulamalari-ve-oyun-dongusu]] — CLI akışları, terminal oyunları ve testlerle desteklenen iş kuralları (kaynak: 2022-03-13-rust-pratikleri-serde-json-ve-biraz-eglence.md) (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- [[oop-ve-polimorfizm]] — Composition, trait'ler, static dispatch ve trait object tabanlı polimorfizm (kaynak: 2022-04-24-rust-pratikleri-oop.md) (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).
- [[state-tasarim-kalibi-ve-durum-gecisleri]] — Trait object ile durum geçişlerini kontrollü yönetme yaklaşımı (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- [[enum-ile-durum-modelleme]] — Enum, state pattern ve typestate ile geçersiz durumları azaltan modelleme yaklaşımı (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md) (kaynak: 2025-02-12-enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi.md).
- [[bellek-optimizasyonu]] — CoW, arena allocator, atomikler ve veri yerleşimi odaklı performans notları (kaynak: 2025-04-03-bellek-yonetiminde-verimlilik-icin-ipuclari-rust-odakli.md) (kaynak: 2025-12-01-rust-ile-kodlama-idmanlari-ileri-seviye.md).
- [[csharp-rust-zig-karsilastirmalari]] — Aynı problem sınıflarının üç dilde farklı çözüm yolları (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md) (kaynak: 2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md).

## Kaynak özetleri

- [[programcidan-programciya-rust]] — Rust'a girişte ownership, bellek güvenliği, `String`/`&str` ve temel veri modeli özeti (kaynak: 2021-12-24-programcidan-programciya-rust.md).
- [[rust-pratikleri-loglama]] — `env_logger` ve log seviyeleriyle terminal loglama pratiği (kaynak: 2022-01-30-rust-pratikleri-loglama.md).
- [[rust-pratikleri-multithreading]] — `thread::spawn` ve `join` ile temel thread akışı (kaynak: 2022-02-06-rust-pratikleri-multithreading.md).
- [[rust-pratikleri-dokumantasyon]] — Dokümantasyon yorumları, `cargo doc` ve doctest kullanımı (kaynak: 2022-02-13-rust-pratikleri-dokumantasyon.md).
- [[rust-pratikleri-channels]] — MPSC, bounded/unbounded kanal ve thread haberleşmesi (kaynak: 2022-02-20-rust-pratikleri-channels.md).
- [[rust-pratikleri-gdb-ile-debug-islemleri]] — GDB ile stack, heap ve pointer gözlemi (kaynak: 2022-02-27-rust-pratikleri-gdb-ile-debug-islemleri.md).
- [[rust-pratikleri-lifetimes-mevzusu]] — Lifetime bildirimi ve `String`-`&str` seçimi (kaynak: 2022-03-06-rust-pratikleri-lifetimes-mevzusu.md).
- [[rust-pratikleri-serde-json-ve-biraz-eglence]] — Serde ile JSON okuma ve CLI filtreleme pratiği (kaynak: 2022-03-13-rust-pratikleri-serde-json-ve-biraz-eglence.md).
- [[rust-pratikleri-http-sunucusu-yazmak-yazmaya-calismak]] — TCP üstünde basit HTTP request/response işleme denemesi (kaynak: 2022-03-20-rust-pratikleri-http-sunucusu-yazmak-yazmaya-calismak.md).
- [[rust-pratikleri-ayni-anda-sadece-tek-bir-degistirilebilir-referans-olabilir]] — Arc, Mutex ve alternatif kilit araçlarıyla güvenli paylaşılan mutasyon (kaynak: 2022-04-03-rust-pratikleri-ayni-anda-sadece-tek-bir-degistirilebilir-referans-olabilir.md).
- [[rust-pratikleri-wordle-oyunu]] — Terminal Wordle örneğinde oyun döngüsü ve testler (kaynak: 2022-04-10-rust-pratikleri-wordle-oyunu.md).
- [[rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak]] — Copy, Clone ve referans geçirme tercihleri (kaynak: 2022-04-17-rust-pratikleri-degiskenleri-kopyalayarak-veya-referans-olarak-tasimak.md).
- [[rust-pratikleri-oop]] — Rust'ta OOP kavramlarının struct, trait ve composition ile yorumu (kaynak: 2022-04-24-rust-pratikleri-oop.md).
- [[rust-pratikleri-trait-objects]] — `dyn Trait` ile heterojen koleksiyon ve runtime polymorphism (kaynak: 2022-05-01-rust-pratikleri-trait-objects.md).
- [[rust-pratikleri-state-tasarim-kalibi]] — State pattern ile durum geçişlerini kontrollü yönetme örneği (kaynak: 2022-05-15-rust-pratikleri-state-tasarim-kalibi.md).
- [[rust-pratikleri-value-moved-here]] — Move semantiği, stack-heap ilişkisi ve sahipliği geri kazanma seçenekleri (kaynak: 2022-05-22-rust-pratikleri-value-moved-here.md).
- [[enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi]] — Rust enum'ları ile servis durum modelleme örneği (kaynak: 2025-02-12-enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi.md).
- [[rust-ve-guvenli-bellek-yonetimi-hakkinda]] — Klasik bellek hataları üzerinden Rust'ın güvenlik yaklaşımı (kaynak: 2025-02-14-rust-ve-guvenli-bellek-yonetimi-hakkinda.md).
- [[bellek-yonetiminde-verimlilik-icin-ipuclari-rust-odakli]] — Bellek verimliliği ve performans için teknikler (kaynak: 2025-04-03-bellek-yonetiminde-verimlilik-icin-ipuclari-rust-odakli.md).
- [[rust-ile-kodlama-idmanlari-baslangic-seviyesi]] — Erken seviye Rust alışkanlıkları ve sık hatalar (kaynak: 2025-10-25-rust-ile-kodlama-idmanlari-baslangic-seviyesi.md).
- [[rust-ile-kodlama-idmanlari-orta-seviye]] — Modüler tasarım, iterator, dönüşüm ve hata yönetimi pratikleri (kaynak: 2025-11-03-rust-ile-kodlama-idmanlari-orta-seviye.md).
- [[rust-ile-kodlama-idmanlari-ileri-seviye]] — Unsafe soyutlamalar, typestate, anyhow ve eşzamanlılık garantileri (kaynak: 2025-12-01-rust-ile-kodlama-idmanlari-ileri-seviye.md).
- [[bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig]] — C#, Rust ve Zig'de metot argümanları, `&mut` ve pointer üzerinden durum değiştirme farkları (kaynak: 2026-01-15-bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig.md).
- [[bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig]] — Çoklu thread ortamında paylaşılan veri yönetimi karşılaştırması (kaynak: 2026-02-15-bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig.md).

## Öğrenme akışı

1. [[programcidan-programciya-rust]]
2. [[rust-ve-guvenli-bellek-yonetimi-hakkinda]]
3. [[sahiplik-ve-borclanma]]
4. [[rust-pratikleri-value-moved-here]]
5. [[rust-pratikleri-lifetimes-mevzusu]]
6. [[rust-pratikleri-multithreading]]
7. [[rust-pratikleri-channels]]
8. [[rust-pratikleri-ayni-anda-sadece-tek-bir-degistirilebilir-referans-olabilir]]
9. [[eszamanlilik-ve-paylasilan-durum]]
10. [[rust-pratikleri-dokumantasyon]]
11. [[rust-pratikleri-loglama]]
12. [[rust-pratikleri-serde-json-ve-biraz-eglence]]
13. [[rust-pratikleri-http-sunucusu-yazmak-yazmaya-calismak]]
14. [[rust-pratikleri-wordle-oyunu]]
15. [[rust-pratikleri-oop]]
16. [[rust-pratikleri-trait-objects]]
17. [[rust-pratikleri-state-tasarim-kalibi]]
18. [[enum-veri-turunun-rust-tarafinda-etkili-bir-kullanimi]]
19. [[enum-ile-durum-modelleme]]
20. [[bellek-yonetiminde-verimlilik-icin-ipuclari-rust-odakli]]
21. [[rust-ile-kodlama-idmanlari-baslangic-seviyesi]]
22. [[rust-ile-kodlama-idmanlari-orta-seviye]]
23. [[rust-ile-kodlama-idmanlari-ileri-seviye]]
24. [[bunu-bir-dene-00-metot-argumanlarinda-degisiklik-c-rust-ve-zig]]
25. [[bunu-bir-dene-01-coklu-thread-ortamlarinda-ortak-veriyi-degistirmek-c-rust-ve-zig]]
