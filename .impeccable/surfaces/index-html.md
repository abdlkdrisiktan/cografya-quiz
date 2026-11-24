---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Quizofya uygulama yüzeyi (index.html)

Scope: tüm uygulama ekranları (ana atölye, kurulum, oyun, geri bildirim, tur sonu, rozetler, ayarlar). Mode: Experience (oyunun içindeki oyuncu). Platform: Android WebView (Capacitor), yatay telefon 844x390 birincil; web masaüstü ikincil.
Audience/job: KPSS adayı, kısa molada haritada yer bulma turu atar, ilerlemesini ve serisini görür.
Constraints: tek dosya, internetsiz, veri sadece cihazda (localStorage), reklamsız, kişisel olmayan metin, kalp emojisi yok.
Memorable moment: doğru cevapta çini sırlanır; konu panosu çini çini dolar.
Unresolved: haptik titreşim eklentisi (Capacitor Haptics) sonraya.

## Direction contract

THESIS: Her yer bir çini; doğru bildikçe çini pişer (bisküvi → astar → sırlı), konu bitince pano tamamlanır. Reddettiği varsayılan: beyaz zemin + yeşil tombul butonlar + XP çubuğu kalıbı.
OWN-WORLD: Kobalt (#1d3f9e) zemin tüm ekranı kaplar, ince çini kafes motifi sadece zeminde. Yüzeyler sırlı beyaz (#f3f7fc), 6px köşe, turkuaz (#14a3a1) çerçeve bandı. Zümrüt doğru, mangan moru yanlış (cezalandırmayan), İznik kırmızısı (#d8392b) ekrandaki tek aktif renk: hedef ve birincil buton. Tek yazı ailesi (Rubik, gömülü), hiyerarşiyi sadece boyut taşır. İkonlar elle çizilmiş SVG.
STORY: Oyuncu açar, seviyesini, serisini ve günün görevini görür; konu panolarındaki çini duvarı neyi bildiğini gösterir; tek dokunuşla hızlı tura ya da yanlış tekrarına girer; her doğru cevapta XP ve kombo ile çini sırlanır.
FIRST VIEWPORT: Üstte seviye madalyonu + unvan + XP bandı, ortada günün görevi, sağda seri alevi ve ayar. Altında solda dört konu panosu yan yana (her biri çini ustalık ızgarası + yıldızlar), sağ sütunda Günün Görevi kartı, kırmızı "Hızlı Tur" birincil buton, turkuaz "Yanlışları Tekrar" ve küçük Rozetler / Bilgi Kartları / Not satırı. Oyun ekranında harita solda turkuaz çerçeveli, sağda soru çinisi.
FORM: İznik Çini Atölyesi, kendi sıralı listemin 6. adayı. seed:98e538b65afc97b0. Raises: VU (aynı boy çinilerden ustalık sırası), Lineup (tek aile, hiyerarşi boyutla), Bebop (sorular arası sert çini dönmesi), Daylight (kırmızı tek aktif renk), Tensegrity (bisküvi/astar/sırlı/çatlak durum sözlüğü).
FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
