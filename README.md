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