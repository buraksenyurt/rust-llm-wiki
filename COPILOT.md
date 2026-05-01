# Rust LLM Wiki

Copilot tarafından yönetilen kişisel bir bilgi tabanı.

## Amaç

Bu wiki, Rust programlama dilini öğrenmek için yapılandırılmış, birbiriyle bağlantılı bir bilgi tabanıdır. Copilot wiki'yi yönetir. Kullanıcı kaynakları derler, sorular sorar ve analizi yönlendirir.

## Klasör Yapısı

```
raw/          -- kaynak belgeler (değiştirilemez -- bunlara asla dokunma)
wiki/         -- Copilot tarafından yönetilen markdown sayfaları
wiki/index.md -- tüm wiki için içindekiler tablosu
wiki/log.md   -- tüm işlemlerin yalnızca ekleme yapılabilen kaydı
```

## İçe Aktarma İş Akışı

Kullanıcı `raw/` klasörüne yeni bir kaynak ekleyip içe aktarmanı istediğinde:

- 1. Kaynak belgenin tamamını oku
- 2. Herhangi bir şey yazmadan önce kullanıcıyla temel çıkarımları tartış
- 3. `wiki/` klasöründe kaynaktan adını alan bir özet sayfası oluştur
- 4. Her önemli fikir veya varlık için kavram sayfaları oluştur ya da güncelle
- 5. İlgili sayfaları birbirine bağlamak için wiki bağlantıları ([[sayfa-adı]]) ekle
- 6. `wiki/index.md` dosyasını yeni sayfalar ve tek satırlık açıklamalarla güncelle
- 7. `wiki/log.md` dosyasına tarih, kaynak adı ve nelerin değiştiğiyle birlikte bir giriş ekle

Tek bir kaynak 10-15 wiki sayfasını etkileyebilir. Bu normaldir.

## Sayfa Biçimi

Her wiki sayfası şu yapıyı izlemelidir:

```markdown
# Sayfa Başlığı

**Özet**: Bu sayfayı açıklayan bir veya iki cümle.

**Kaynaklar**: Bu sayfanın dayandığı ham kaynak dosyaların listesi.

**Son güncelleme**: En son güncelleme tarihi.

---

## İlgili sayfalar

- [[ilgili-kavram-1]]
- [[ilgili-kavram-2]]
```

## Alıntı Kuralları

- Her olgusal iddia kendi kaynak dosyasına atıfta bulunmalıdır
- İddianın ardından (kaynak: dosyaadı.md) biçimini kullan
- İki kaynak çelişiyorsa çelişkiyi açıkça belirt
- Kaynağı olmayan bir iddiayı doğrulama gerektirir olarak işaretle

## Soru Yanıtlama

Kullanıcı bir soru sorduğunda:

1. İlgili sayfaları bulmak için önce `wiki/index.md` dosyasını oku
2. Bu sayfaları oku ve bir yanıt sentezle
3. Yanıtında belirli wiki sayfalarına atıfta bulun
4. Yanıt wiki'de yoksa bunu açıkça belirt
5. Yanıt değerliyse yeni bir wiki sayfası olarak kaydetmeyi teklif et

İyi yanıtlar zamanla birikmesi için wiki'ye geri eklenmelidir.

## Denetim

Kullanıcı wiki'yi denetlemeni veya lint yapmanı istediğinde:

- Sayfalar arasındaki çelişkileri kontrol et
- Sahipsiz sayfaları bul (diğer sayfalardan gelen bağlantısı olmayanlar)
- Sayfalarında geçen ama kendi sayfası olmayan kavramları belirle
- Daha yeni kaynaklara göre güncelliğini yitirmiş olabilecek iddiaları işaretle
- Tüm sayfaların yukarıdaki sayfa biçimine uyup uymadığını kontrol et
- Bulguları önerilen düzeltmelerle birlikte numaralı liste olarak raporla

## Kurallar

- `raw/` klasöründeki hiçbir şeyi asla değiştirme
- Değişikliklerden sonra her zaman `wiki/index.md` ve `wiki/log.md` dosyalarını güncelle
- Sayfa adlarını küçük harfle ve tire ile yaz (örn. `makine-ogrenimi.md`)
- Açık ve sade bir dil kullan
- Bir şeyin nasıl kategorilendirileceğinden emin değilsen kullanıcıya sor
