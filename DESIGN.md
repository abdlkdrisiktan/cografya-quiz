---
name: Quizofya
description: KPSS coğrafyası için harita odaklı, oyunlaştırılmış tekrar oyunu. Görsel dünya İznik çini atölyesi.
colors:
  iznik-cobalt: "#1d3f9e"
  cobalt-deep: "#132c73"
  ink-navy: "#0e1f55"
  ink-soft: "#3d4f86"
  turquoise-glaze: "#14a3a1"
  turquoise-ink: "#0c7d7b"
  turquoise-tint: "#d3efee"
  emerald-glaze: "#1f8a4c"
  emerald-tint: "#dcf1e3"
  bolus-red: "#d8392b"
  bolus-red-deep: "#9a2318"
  manganese: "#7a3b69"
  manganese-tint: "#f1e2ec"
  frit-white: "#f3f7fc"
  bisque: "#e7d6bf"
  bisque-line: "#cdb79a"
  sea: "#d4e9f3"
  hairline: "#c9d6ea"
typography:
  display:
    fontFamily: "Rubik, system-ui, sans-serif"
    fontSize: "52px"
    fontWeight: 900
    lineHeight: 0.95
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Rubik, system-ui, sans-serif"
    fontSize: "26px"
    fontWeight: 900
    lineHeight: 1.05
  title:
    fontFamily: "Rubik, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 800
    lineHeight: 1.15
  body:
    fontFamily: "Rubik, system-ui, sans-serif"
    fontSize: "13.5px"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "Rubik, system-ui, sans-serif"
    fontSize: "12.5px"
    fontWeight: 700
    lineHeight: 1.3
rounded:
  tile: "2px"
  chip: "4px"
  surface: "6px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
components:
  button-primary:
    backgroundColor: "{colors.bolus-red}"
    textColor: "{colors.frit-white}"
    rounded: "{rounded.surface}"
    padding: "13px 14px"
  button-secondary:
    backgroundColor: "{colors.turquoise-ink}"
    textColor: "{colors.frit-white}"
    rounded: "{rounded.surface}"
    padding: "13px 14px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink-navy}"
    rounded: "{rounded.surface}"
    padding: "13px 14px"
  surface-card:
    backgroundColor: "{colors.frit-white}"
    textColor: "{colors.ink-navy}"
    rounded: "{rounded.surface}"
    padding: "11px 13px"
  pill:
    backgroundColor: "#ffffff"
    textColor: "{colors.ink-navy}"
    rounded: "{rounded.surface}"
    padding: "8px 11px"
  pill-active:
    backgroundColor: "{colors.iznik-cobalt}"
    textColor: "#ffffff"
  option-button:
    backgroundColor: "{colors.frit-white}"
    textColor: "{colors.ink-navy}"
    rounded: "{rounded.surface}"
    padding: "9px 11px"
  category-tag:
    textColor: "#ffffff"
    rounded: "{rounded.chip}"
    padding: "3px 7px"
---

# Design System: Quizofya

## Overview

**Creative North Star: "İznik Çini Atölyesi"**

Her yer bir çinidir. Oyuncu doğru bildikçe çini pişer: önce bisküvi (henüz görülmedi), sonra astar (öğreniliyor), sonra sırlı (öğrenildi). Yanlış cevap çiniyi çatlatır, tekrar turu onu onarır. Bir konunun bütün çinileri sırlanınca pano tamamlanır. Ana ekran bu panoların duvarıdır; neyi bildiğin, hiçbir yazı okumadan renkten anlaşılır.

Zemin baştan sona İznik kobaltıdır ve üzerinde çok ince bir çini kafesi durur. Yüzeyler sırlı beyaz (frit) levhalardır, üstlerinde konunun sır rengiyle 7–8 px'lik bir bant taşırlar. Harita her zaman turkuaz bir çerçevenin içindedir ve ekranın en büyük nesnesidir. Enerji parlak ve doygundur, ama tek bir kuralla düzenlenir: kırmızı sadece aktif olana aittir.

**Key Characteristics:**
- Kobalt zemin tüm ekranı kaplar; süsleme (kafes, 8 köşeli yıldız) sadece zeminde ve madalyonda.
- Sırlı beyaz levhalar, küçük köşe (6 px), üstte konu renginde sır bandı.
- Çini durumları ilerlemenin kendisidir: bisküvi, astar, sırlı, çatlak.
- Tek yazı ailesi (Rubik, gömülü); hiyerarşiyi boyut ve ağırlık taşır.
- İkonlar elle çizilmiş 2.2 px çizgili SVG; emoji sadece metin içinde ses tonu için.

## Colors

Kobaltın her yeri kapladığı, turkuaz ve zümrütün sır gibi parladığı, mercan kırmızısının nadir olduğu tam bir İznik paleti.

### Primary
- **İznik Kobaltı** (#1d3f9e): Uygulama zemini, aktif hap (pill) dolgusu, harita kıyı çizgisi. Ekranın en az %60'ı.
- **Derin Kobalt** (#132c73): Zemin üstündeki koyu kontroller (ikon butonları, mini butonlar, XP çubuğu yuvası).

### Secondary
- **Turkuaz Sır** (#14a3a1): Harita çerçevesi, XP dolgusu, kazanılmış yıldızlar, seviye madalyonunun dış yıldızı, Şehir Bulmaca'nın sır rengi. Dekoratif ve büyük alanlarda.
- **Turkuaz Mürekkep** (#0c7d7b): Üzerinde beyaz yazı taşıyan turkuaz dolgular (ikincil buton, kombo çipi, seri çipi, göl etiketi). Kontrast için Turkuaz Sır'ın yerine geçer.

### Tertiary
- **İznik Kırmızısı / Bolus** (#d8392b): Sadece birincil eylem butonu ve haritadaki hedef (yanıp sönen nokta, işaretli il). Gölgesi #9a2318.
- **Zümrüt Sır** (#1f8a4c): Doğru cevap, sırlanmış işaret, Göl-Dağ-Ova-Baraj sır rengi.
- **Mangan Moru** (#7a3b69): Yanlış cevap ve çatlak çini. Cezalandırmayan bir hata rengidir; kırmızı yanlışa asla kullanılmaz. Boru hatları sır rengi.

### Neutral
- **Frit Beyazı** (#f3f7fc): Bütün levha yüzeyleri.
- **Lacivert Mürekkep** (#0e1f55): Levha üstündeki ana metin. **Yumuşak Mürekkep** (#3d4f86): ikincil metin.
- **Bisküvi** (#e7d6bf, çizgi #cdb79a): Henüz görülmemiş çini.
- **Deniz** (#d4e9f3): Harita denizi. **Kılçizgi** (#c9d6ea): Hap ve kart kenarları.

### Named Rules
**The Tek Kırmızı Rule.** İznik kırmızısı ekrandaki tek aktif renktir: birincil buton ve haritadaki hedef. Madalyon, yıldız, seri, bant ya da hata için asla kullanılmaz.

**The Çatlak Mor Rule.** Yanlış cevap ve çatlak çini her zaman mangan morudur. Hata öğrenmenin parçasıdır, alarm değildir.

**The Mürekkep Turkuaz Rule.** Üzerinde 18 px altı beyaz yazı olan her turkuaz dolgu #0c7d7b'dir; parlak #14a3a1 sadece yazısız sır alanlarında kalır.

## Typography

**Display Font:** Rubik (variable 300–900, latin + latin-ext alt kümeleri base64 olarak gömülü; yedek system-ui)
**Body Font:** Rubik
**Label Font:** Rubik

**Character:** Hafif yuvarlak köşeli, kalın ağırlıklarda tok bir grotesk. Türkçe karakterleri (ğ, ş, ı, İ) eksiksiz taşır. Sayılar tablo hizalıdır (`font-variant-numeric: tabular-nums`).

### Hierarchy
- **Display** (900, 52 px, 0.95, -0.03em): Tur sonu skoru. Seviye atlama madalyonundaki rakam (40 px).
- **Headline** (900, 26 px, 1.05): Soru kartındaki yer adı; 22 karakteri aşan adlar 19 px'e iner. Pencere başlıkları 18–21 px.
- **Title** (800, 14.5–17 px): Pano adı, buton etiketi, görev başlığı, geri bildirim başlığı.
- **Body** (400–500, 13.5–14.5 px, 1.45): Açıklamalar ve bilgi kartları.
- **Label** (700–800, 11.5–13 px): Kategori etiketi, sayaçlar, "x/y sırlı".

### Named Rules
**The Tek Aile Rule.** Bütün metin Rubik'tir. Hiyerarşiyi sadece boyut ve ağırlık taşır; ikinci bir yazı ailesi ya da büyük harf izleme etiketi yoktur.

**The Başlık Üstü Etiket Yok Rule.** Soru adının ya da başlığın üstüne eyebrow/kicker satırı konmaz. Soru cümlesi adın altında, kategori etiketinin yanında durur.

## Layout

Birincil hedef yatay telefondur (844×390, 740×360'a kadar). İki sütun:
- **Ana ekran:** solda dört pano (`repeat(4, 1fr)`, 10 px aralık), sağda 262 px'lik eylem sütunu.
- **Oyun ekranı:** solda harita, sağda 310 px soru sütunu.
- **Tur sonu:** iki eşit levha.

Yatay telefonda `#app` tam ekran yüksekliğine kilitlenir (`100dvh`). Taşan içerik sadece kendi sütununda kayar; Devam butonu yapışkandır (sticky).

Masaüstünde (≥900×600) içerik dikeyde ortalanır ve panolar içerik yüksekliğindedir. Dikey dar ekranda (≤720 px portrait) her şey tek sütuna, panolar 2×2'ye düşer.

Ritim 4/8/12/16 px'tir. Güvenli alan boşlukları (safe-area) her kenarda korunur.

## Elevation & Depth

Derinlik iki katmandır: kobalt zemin ve onun üstünde duran sırlı levhalar.
- **Levha gölgesi** (`--lift`), ofsetli ve yumuşaktır: `0 2px 0 rgba(14,31,85,.25), 0 8px 18px -8px rgba(5,14,45,.55)`.
- **Butonlar** basılabilir bir çini gibi alt kenar gölgesi taşır: `0 4px 0` + kendi koyu tonu. Basınca 3 px aşağı iner.
- **Pencereler**, zemini `rgba(8,18,52,.62)` ile karartır.

### Named Rules
**The Sır Bandı Rule.** Levhanın kimliği üstteki iç bant ile verilir (`inset 0 7px 0 <konu rengi>`). Kenar çizgisi ya da yan şerit kullanılmaz.

## Shapes

- Levha ve buton köşeleri küçüktür (6 px), çünkü çiniler keskin kesilir. Etiketler 4 px, ızgaradaki çiniler 2 px.
- İmza biçim İznik'in **sekiz köşeli yıldızıdır**: iki kare, biri 45° döndürülmüş. Seviye madalyonu iki katmanlıdır: turkuaz dış yıldız, frit iç yıldız, kobalt rakam. Rozet madalyonları ve yıldızlar da aynı biçimdedir.
- Can (hak) göstergesi 45° döndürülmüş küçük bir çini karosudur; kalp kullanılmaz.

## Components

### Buttons
- **Shape:** 6 px köşe, alt kenar gölgesi.
- **Primary:** İznik kırmızısı dolgu, beyaz 800 ağırlık yazı. Ekranda tek bir tane bulunur: Oyuna Başla, Hızlı Tur, Devam, Tekrar Oyna.
- **Secondary:** Turkuaz mürekkep dolgu (#0c7d7b), gölge #054a49. "Yanlışları Tekrar" gibi. Pasif hali #5d75b8.
- **Ghost:** Şeffaf, 2 px iç kılçizgi; frit üstünde lacivert yazı.
- **Focus:** 3 px #ffd9d4 dış halka.

### Pano (imza bileşen)
Konu başına bir frit levha:
- Üstte konu renginde sır bandı, altında ad ve "x/y sırlı · %en iyi" satırı.
- Ortada konunun bütün öğeleri çini ızgarası olarak durur: geçitlerde 5, doğada 6, hatlarda 5, illerde 9 sütun.
- Altta üç yıldız ve konu renginde "Oyna" çipi.
- 150 px'ten dar olunca yıldızlar küçülür ve çip sadece ikona döner (container query).

### Çini durumları
- **t0 Bisküvi:** #e7d6bf, iç çizgi #cdb79a.
- **t1 Astar:** Beyaz zemin, iki köşesinde konu rengi.
- **t2 Sırlı:** Düz konu rengi ve sol üstte beyaz parıltı.
- **t3 Çatlak:** Bisküvi üstünde çapraz mangan çizgi.

### Soru kartı ve geri bildirim
- **Soru kartı:** Frit levha, konu bandı. Yer adı headline boyutunda; altında kategori etiketi ve soru cümlesi.
- **Geri bildirim kartı:** Zümrüt (doğru) ya da mangan (yanlış) bant. Yanında sırlanma parıltısıyla açılan sonuç çinisi ve turkuaz tint üstünde "+XP ×kombo" çipi.
- **Cevap verildikten sonra** soru kartı tek satıra küçülür.

### Haplar ve seçimler
- **Hap (pill):** Beyaz, 2 px kılçizgi. Aktif olanı kobalt dolgu.
- **Oyun modu seçimi:** İkon + başlık + açıklama içeren karttır. Aktif olanı kobalt kenar ve #e7eefb dolgu alır.
- **Anahtar (switch):** Açıkken turkuaz.

### Üst çubuk (HUD)
- **Ana ekran:** Madalyon, unvan, "XP / gereken", turkuaz XP çubuğu, seri çipi (o gün oynandıysa turkuaz mürekkep) ve ayar butonu.
- **Oyun ekranı:** Çıkış butonu ve tur çini sırası (soru başına 18×14 px kare: doğru zümrüt, yanlış mangan, şimdiki beyaz; 30 sorudan fazlasında çubuk). Yanında kombo çipi, can karoları ve skor.

### Motion
- Soru geçişi sert bir çini dönmesidir (`rotateX(-80deg)` → 0, 340 ms).
- Doğru cevapta sonuç çinisinden bir sır parıltısı geçer.
- Kombo çipi zıplar. Yıldızlar sırayla döner.
- Seviye madalyonu dönerek büyür. Konfeti küçük kare çinilerdir.
- Kolaylık eğrisi `cubic-bezier(.16,1,.3,1)`. `prefers-reduced-motion` hepsini kapatır.

## Do's and Don'ts

### Do:
- **Do** zemini her ekranda İznik kobaltı (#1d3f9e) ve kafes deseniyle doldur.
- **Do** yeni bir konu grubu eklerken ona bir sır rengi ver ve panoda çini ızgarasıyla göster.
- **Do** ilerlemeyi çini durumlarıyla anlat (bisküvi, astar, sırlı, çatlak). Yüzde halkası ya da sparkline kullanma.
- **Do** haritayı turkuaz çerçevede, ekranın en büyük nesnesi olarak tut.
- **Do** ikonları `<symbol>` sprite'ına 24×24, 2.2 px çizgili SVG olarak ekle.

### Don't:
- **Don't** kırmızıyı madalyon, yıldız, seri, bant ya da yanlış cevap için kullanma (Tek Kırmızı kuralı).
- **Don't** yanlış cevabı kırmızıyla gösterme; mangan moru kullan.
- **Don't** başlıkların üstüne kicker/eyebrow satırı koyma.
- **Don't** emoji ya da Unicode glifini ikon yerine kullanma; emoji sadece ses tonu için metin içinde kalır.
- **Don't** kalp simgesi kullanma (can göstergesi çini karosudur). Bu, PRODUCT.md'deki kişisel olmama kararından gelir.
- **Don't** harici font ya da ağ isteği ekleme. Font dosyaya gömülüdür ve uygulama internetsiz çalışır.
