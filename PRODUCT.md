# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

Tek bir web uygulaması (`index.html`) iki şekilde yayınlanıyor: tarayıcıda çalışan web sürümü ve Capacitor ile paketlenmiş Android uygulaması **Quizofya** (`tr.com.quizofya`). Android sürümü native bir tasarım dili kullanmıyor; aynı web arayüzü bir WebView içinde çalışıyor.

## Users

KPSS'ye hazırlanan adaylar. Kullanıcılar coğrafya konularını, özellikle haritada yer bulmayı ve tanımayı çalışıyor. Kitaptan ya da ezberden çalışmak yerine görsel hafızayla, kısa oyun turlarıyla tekrar yapıyorlar. Uygulama çoğunlukla telefonda, yatay ekranda, çalışma araları gibi kısa oturumlarda kullanılıyor.

## Product Purpose

KPSS coğrafyasındaki harita bilgisini oyunlaştırılmış tekrarla kalıcı hale getirmek. Kullanıcı bir yerin adını görüp haritada işaretliyor ya da işaretli yerin adını seçiyor. Her cevaptan sonra kısa bir açıklama alıyor. Başarı ölçütü şu: kullanıcı sınavda harita sorularında doğru yeri tanıyabiliyor ve çalışma süreci yorucu değil, motive edici geçiyor.

## Positioning

Ücretsiz, reklamsız ve tamamen harita odaklı bir KPSS coğrafya çalışma aracı. Sınav için önemli olan noktaların gerçek konumları gerçek bir Türkiye haritası üzerinde sorulur. Hesap gerektirmez, internetsiz çalışır ve kullanıcıdan hiçbir veri toplamaz.

## Operating Context

- **Ana ekran (atölye):** Seviye, XP, günlük seri ve günün görevi üstte. Dört konu panosu, her öğeyi bir çini olarak gösteriyor (bisküvi: görülmedi, astar: öğreniliyor, sırlı: öğrenildi, çatlak: tekrar lazım). Sağda Hızlı Tur, Yanlışları Tekrar, Rozetler, Bilgi Kartları ve Günün Notu var.
- **Bir oyun turu:** Kullanıcı bir panoya dokunup konu, oyun modu, harita görünümü ve isteğe bağlı can modunu (3 hak) seçiyor. Sorular karışık sırayla geliyor. Her cevaptan sonra geri bildirim kartı XP ve kombo ile çıkıyor. Tur sonunda skor, yıldızlar, kazanılan XP, yeni rozetler ve tekrar edilecekler gösteriliyor.
- **Hızlı Tur:** Her konudan 10 karışık soru. Henüz sırlanmamış çinilere öncelik veriyor.
- **Yanlışları Tekrar:** Çatlak çinilerden en fazla 15 soruluk bir tur. Doğru cevap çatlağı onarıyor.
- **Oyunlaştırma:**
  - XP ve seviye. Unvanlar: Harita Çırağı, Kalfası, Ustası, Nakkaş, Başusta, Atlas Üstadı.
  - Kombo çarpanı: 3, 6 ve 10 doğruda ×1.5, ×2, ×3.
  - Günlük seri. Her 7 günde bir kalkan kazanılıyor, en fazla 2 tane.
  - Günün görevi: +30 XP.
  - Konu başına 3 yıldız ve 16 rozet.
- **Harita görünümleri:**
  - Türkiye haritası (il sınırları olmadan)
  - Siyasi harita, il isimleri olmadan
  - Siyasi harita, il isimleriyle
- **Soru grupları:**
  - Geçitler ve sınır kapıları: 10 tünel/geçit ve 15 sınır kapısı
  - Göl, dağ, ova ve baraj: 26 soru
  - Petrol ve doğalgaz hatları: 10 soru
  - Şehir Bulmaca: 81 il, bölgelere göre filtrelenebiliyor
- **Oyun modları:**
  - **Haritada Bul:** İsim verilir, kullanıcı haritada yeri işaretler.
  - **İsmini Bil:** Yer haritada işaretlidir, kullanıcı ismi şıklardan seçer.
- **Bilgi Kartları:** Konuların özeti, oyundan önce çalışmak için.
- **Bugünün Motivasyon Notu:** KPSS adaylarına yönelik kısa motivasyon metinleri.
- **Telefonda kullanım:** Uygulama yatay ekrana kilitli. Haritada iki parmakla yakınlaştırma, kaydırma ve − / + / ⟲ düğmeleri var. Bir dokunuş, parmak kalkınca ve kaydırma yapılmadıysa cevap sayılıyor. Android geri tuşu sırasıyla açık pencereyi kapatıyor, oyundan çıkmayı soruyor ya da ana menüye dönüyor.

## Capabilities and Constraints

- **Tek dosya:** Tüm uygulama (HTML, CSS, JS, harita verisi ve base64 gömülü Rubik fontu) tek bir `index.html` içinde. Dış kütüphane ya da ağ isteği yok, internetsiz çalışıyor. Görsel sistem `DESIGN.md` dosyasında.
- **Android paketleme:** Capacitor 8 ile yapılıyor.
  - `dev` flavor: `tr.com.quizofya.dev`, uygulama adı "Quizofya Dev"
  - `prod` flavor: `tr.com.quizofya`, Play Store sürümü
- **Harita verisi:** Önceden projekte edilmiş SVG koordinatları kullanılıyor (`viewBox 0 0 920 400`). Cevap kontrolü harita birimleriyle yapılıyor:
  - Nokta soruları: 40 birim tolerans
  - Boru hattı soruları: 16 birim tolerans
  - İl soruları: dokunulan ilin adına göre
- **Kapsam:** Sadece KPSS coğrafyası ve harita odaklı. Yeni içerik haritada yer bulma/tanıma konularıyla genişler (ör. akarsular, madenler, tarım ürünleri). Harita dışı bilgi soruları ve başka dersler kapsam dışında.
- **Veri:** Hesap yok. İlerleme (XP, çini durumları, seri, rozetler, ayarlar) sadece cihazda, `localStorage` içinde `quizofya.v1` anahtarıyla saklanıyor (kullanıcı kararı, 2026-11-24). Hiçbir veri gönderilmiyor ve analitik yok. Buluta senkron ya da hesap eklemek yeni bir ürün kararı gerektirir.
- **Gelir:** Tamamen ücretsiz ve reklamsız. Reklam, ödeme ya da premium özellik eklenmeyecek.
- **Dil:** Sadece Türkçe.

## Brand Commitments

- **İsim:** Quizofya
- **İkon:** Kırmızı zemin üzerinde krem rengi Türkiye silueti ve Ankara'da bir pin. Kaynak görseller `assets/` klasöründe.
- **Ses tonu:** Sıcak, cesaretlendirici ve hafif esprili, "sen" diye hitap ediyor. Yanlış cevapta suçlamıyor, "artık biliyorsun" diyerek öğrenmeye çeviriyor. Emoji kullanılıyor.
- **Kişisel olmama:** Metinler herkese hitap etmeli. Kişisel, romantik ya da cinsiyete özgü ifadeler, kalp emojileri ve kişi imzası kullanılmıyor. Bu, kullanıcının açık kararı.

## Evidence on Hand

- Gerçek içerik: `index.html` içindeki soru verisi, açıklamalar, bilgi kartları ve motivasyon metinleri.
- Kullanıcı yorumu, indirme sayısı, başarı istatistiği, basın ya da kurum onayı **yok**. Bunlar uydurulmamalı.

## Product Principles

1. **Harita her şeyin merkezinde.** Her soru gerçek bir konumu öğretir. Haritayı küçülten, kapatan ya da ondan dikkat dağıtan her şey ürünün aleyhine çalışır.
2. **Yanlış cevap öğrenmenin parçası.** Her cevaptan sonra doğru yer gösterilir ve kısa bir açıklama verilir. Ton motive edicidir, cezalandırıcı değildir.
3. **Adil cevap.** Kullanıcının bilgisi ölçülür, parmak isabeti değil. Yanlışlıkla dokunma, kaydırma ya da küçük ekran yüzünden yanlış sayılmamalı.
4. **Sıfır sürtünme, sıfır veri.** Hesap yok, reklam yok, internet gerekmiyor. Açılır ve hemen çalışılır.
5. **Kısa oturuma uygun.** Bir tur birkaç dakikada başlayıp bitebilmeli. Her an ana menüye dönülebilmeli.
