# 🗂️ Arşiv - Akıllı Dosyalama Asistanı

**Arşiv**, kişisel belgelerinizi, ders notlarınızı, fatura ve makbuzlarınızı sıradan klasörler yerine **görsel ve etkileşimli** bir şekilde organize etmenizi sağlayan akıllı bir dosyalama ve not tutma asistanıdır. 

Sıradan bir liste görünümü yerine; belgelerinizi 3 boyutlu bir defterde okuyabilir, zaman tünelinde geçmişe yolculuk yapabilir, çalışma masanızda kartları serbestçe düzenleyebilir veya belgeler arası ilişkileri bir bilgi ağı (graph) üzerinde keşfedebilirsiniz.

## 🌟 Öne Çıkan Özellikler

*   **Çoklu Görünüm Seçenekleri:**
    *   **🗂️ Klasörler (Scrapbook):** Belgeleri estetik bir mantar pano / albüm hissiyatıyla listeleme.
    *   **📔 3D Defter:** Notları ve günlükleri üç boyutlu, sayfa çevirme animasyonlu gerçek bir defter gibi okuma.
    *   **🕰️ Zaman Tüneli:** Fatura ve makbuz gibi tarihsel önemi olan belgeleri kronolojik bir tünelde 3D olarak kaydırarak inceleme.
    *   **🕸️ Bilgi Ağı:** Belgeler arasındaki ortak etiketlere dayalı ilişkileri, fizik motoru destekli bir ağ (graph) üzerinde görselleştirme.
    *   **📌 Çalışma Masası:** Belgeleri serbestçe sürükleyip bırakabileceğiniz interaktif bir pano.
*   **Karanlık / Aydınlık Tema:** Sistem tercihinize göre otomatik ayarlanan, manuel olarak da değiştirilebilen arayüz.
*   **Görsel ve Metin Birlikteliği:** Belgelere resim yükleme ve not ekleme özelliği.

## 🚀 Kurulum Adımları

Bu proje **tek bir HTML dosyası** (`Arsiv_Scrapbook.html`) içerisine yerleştirilmiş (Single-File) statik bir web uygulamasıdır. Herhangi bir sunucuya, veritabanı kurulumuna veya derleme (build) işlemine ihtiyacınız yoktur.

1.  Proje dizinindeki `Arsiv_Scrapbook.html` dosyasını bilgisayarınıza indirin.
2.  Dosyaya çift tıklayarak modern bir web tarayıcısında (Google Chrome, Safari, Mozilla Firefox, Microsoft Edge vb.) açın.
3.  Uygulama anında çalışmaya başlayacaktır!

*(Not: Uygulama şu an için verileri tarayıcı hafızasında (in-memory) tutmaktadır, sayfayı yenilediğinizde eklediğiniz geçici belgeler sıfırlanır.)*

## 💻 Kullanılan Teknolojiler

Proje, herhangi bir dış kütüphane veya framework (React, Vue, Tailwind vb.) kullanılmadan, tamamen web standartları ile geliştirilmiştir:

*   **HTML5:** Semantik yapı ve SVG ikon mimarisi (örn. kurbağa maskotu).
*   **CSS3:** 
    *   Kapsamlı Custom Properties (Değişkenler) ile tema yönetimi.
    *   CSS Grid & Flexbox ile modern mizanpaj.
    *   Gelişmiş `transform` (3D döndürme, perspektif) ve `animation` kuralları.
*   **Vanilla JavaScript (ES6+):** 
    *   DOM manipülasyonu, olay dinleyicileri (pointer events).
    *   Fizik tabanlı animasyonlar (Bilgi ağındaki node'ların çekim/itme kuvvetleri `requestAnimationFrame` ile işlenmiştir).

## 🤖 Yapay Zeka Entegrasyonu

Uygulamanın vizyonu, yüklenen belgeleri manuel bir çabaya gerek kalmadan organize etmektir. Proje mimarisi yapay zeka (YZ) entegrasyonuna hazır olarak tasarlanmıştır.

### Projede Yapay Zekanın Konumu ve Aşamaları:
1.  **Otomatik Sınıflandırma ve Etiketleme:** 
    *   *Mevcut Durum:* Metin içeriğine bakarak basit RegEx tabanlı kural setleriyle sınıflandırma (Fatura, Not, Makbuz vb.) ve etiketleme (`classify` ve `autoTags` fonksiyonları) yapılmaktadır.
    *   *Gelecek Planı:* LLM (Büyük Dil Modelleri) kullanılarak metnin bağlamı anlaşılacak, dökümanın türü kusursuz tespit edilecek ve anlamsal etiketler (örn. "vize konuları", "aylık gider") otomatik üretilecektir.
2.  **Optik Karakter Tanıma (OCR):**
    *   *Gelecek Planı:* Kullanıcı bir fiş veya not fotoğrafı yüklediğinde, görseldeki metinler OCR modelleri ile otomatik olarak çıkarılıp dökümanın metin alanına yazılacaktır. (Arayüzde OCR tarama animasyon katmanı halihazırda tasarlanmıştır).
3.  **RAG (Retrieval-Augmented Generation) ile Anlamsal Arama:**
    *   Uygulama içindeki belgelerde (notlar, araştırmalar) anahtar kelime yerine, anlam tabanlı (vektörel) arama yapılması ve kullanıcının belgelerine sorular sorarak özetleyici yanıtlar alabilmesi hedeflenmektedir.

### 🧠 Geliştirme Sürecinde Yapay Zeka Kullanımı
Bu projenin fikirsel taslağının oluşturulması, kompleks CSS 3D animasyonlarının kurgulanması, fizik motorunun yazılması ve genel kod mimarisinin (Vanilla JS & Tek dosya yapısı) geliştirilmesi süreçlerinde **Claude** yapay zeka modelinden aktif olarak yararlanılmıştır. Claude, projenin hem yaratıcı arayüz tasarımında hem de teknik problem çözümünde bir eş-geliştirici (co-developer) olarak görev almıştır.
