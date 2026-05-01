# rust-llm-wiki

Andrej Karpathy'nin LLM Wiki önerisini Copilot ile denediğim çalışma alanı.

Bu çalışmada Obsidian ve Copilot CLI kullanılmakta. Karpathy kendi LLM wiki örneğinde doğal olarak Claude için hazırlanmış bir markdown dosyası ve CLI aracını kullanmakta. Benzer bir çalışmayı Microsoft Copilot ile denemeye çalışıyorum.

## Amaç

Rust ile ilgili yazdığım blog yazılarını baz aldığım minik bir LLM wiki oluşturmak. Doküman içerikleri ve anlamsal ilişkileri wiki olarak özetletmek. Copilot komut satırını kullanarak bu arşive sorular sorabilmek. **RAG** kurgusunun **LLM Wiki** olarak işletilmesini sağlamak.

## Hazırlıklar

Kaynaklardan hareketle üç klasör oluşturdum. 

```text
/raw -- Tüm makale içerikleri (görselleri ile birlikte) burada yapılandırılıyor
/templates -- Şablonlar gerekliyorsa burada olacak
/wiki -- Hem indekslenmiş wiki içerikleri hem de güncelleme logları burada tutuluyor
COPILOT.md -- Normalda CLAUDE.md olarak yazılan talimatların yer aldığı dosya
```

## Denemeler

Daha sonra Copilot CLI arabiriminden `\init` komutunu kullanarak `.github\copilot-instructions.md` dosyasını oluşturdum. Copilot özellikle `COPILOT.md` içeriğine bakarak gerekli düzenlemeleri yaptı. Ardından şu promptu kullandım.

```text
raw klasöründeki makaleleri oku ve wiki'yi güncelle.
```

![[Runtime_00.png]]

Sonrasında şu soruyu sordum.

```text
Rust ve zig dillerinde değişkenler nasıl tanımlanır? Farklar nelerdir?
```

Buradaki dikkat edilmesi gereken nokta ajanın doğrudan makaleleri araştırmak yerine öncelikle wiki içeriğine gitmesidir.

![[Runtime_01.png]]

Hatta kendince bir özeti de buradaki içeriklere göre çıkartmış durumda.

![[Runtime_02.png]]

Tabii burada ajanın raw içerisindeki bilgilere bakarak bir sonuç ürettiğini ve oradaki bilgilerin doğruluğuna göre bu sonuçların değerlendirilmesi gerektiğini unutmayalım. 

`raw` klasörüne yeni bir içerik eklediğimizde de `wiki` içeriğini güncelletebiliriz. Bununla birlikte `wiki` içeriğinin sağlıklık kalması için `linting` işlemi de uygulatabiliriz. 

```text
Wiki içeriklerinde lint işlemini uygula.
```

Buna göre `Copilot` wiki içeriklerindeki bağlantıları, formatlamayı kontrol edecek ve gerekli düzeltmeleri yapacaktır.

![[Runtime_03.png]]

Bu kullanımda işin güzel yanı içerikteki ilişkilerin **Obsidian** üzerinden grafiksel olarak gösterimidir. Ortada bir vektör veritabanı, maliyetli rag hattı, embedding işlemleri vs olmadığına dikkat edelim.

![[Runtime_04.png]]
