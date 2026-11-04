# Arthyra Studio — geliştirici ve gizlilik sitesi

GitHub Pages için buildless HTML/CSS sitesi. Yayıncı Arthyra Studio; ilk uygulama Güne Bir Söz. Mobil uygulama kaynakları bu depoya kopyalanmaz.

- `site.json`: genel site adresi, kullanıcı tarafından seçilecek herkese açık destek e-postası, politika tarihi.
- `generate.py`: ana sayfa, TR/EN gizlilik HTML'leri, `404.html`, `sitemap.xml` ve `robots.txt` üretir. Canonical, hreflang ve Open Graph adresleri `site.json` `base_url`'den gelir; sayfa içi bağlantılar göreli (404 hariç: her yolda sunulduğu için kökten mutlak).
- `docs/assets/og-image.jpg`: 1200×630 paylaşım önizlemesi; `../marka/arthyra-studio/google-play-ust-bilgi-4096x2304.jpg`'den kırpıldı.
- `docs/`: GitHub Pages yayın kökü; CSS ve yerel marka görselleri burada.
- `docs/gunebirsoz/sozler-v1.json`: Güne Bir Söz 1.1.2+ uygulamasının indirdiği söz kataloğu (CC BY-SA 4.0, Vikisöz'den). Elle düzenleme; `../gunluk-alinti/scripts/build-quote-catalog.mjs` üretir, sonra burada commit/push. Yolu ve `format` alanını değiştirmek yayındaki uygulamaları bozar; yeni biçim için `sozler-v2.json` ekle.
- `docs/CNAME`: özel alan adı `arthyrastudio.info`. Silme; üretici dokunmaz. DNS Squarespace'te (GitHub Pages A/AAAA, `www` CNAME, `_github-pages-challenge-onrart` doğrulama TXT); Google Workspace MX/SPF/DKIM/DMARC kayıtlarına dokunma.
- `GUNCEL_DURUM.md`: güncel durum ve sonraki adım. `docs/` içine koyma; orası herkese açık yayın köküdür.

Komutlar: `python generate.py` yerel taslak üretir; `python generate.py --publish` iletişim e-postası eksikse durur. `python -m http.server 8787 --bind 127.0.0.1 --directory docs` yerel önizleme.

Gizlilik metni gerçek uygulama koduyla tutarlı tutulmalı. Yeni analitik/reklam, veri aktarımı, hesap veya hizmet eklenirse metni güncelle. Cihaz yedeklemesini yokmuş gibi anlatma: uygulamada Android allowBackup=true. İletişim adresini kullanıcı seçmeden yayınlama. GitHub Pages hedefi `onrart/arthyra-studio`, dal main, kaynak /docs. Diğer projelerin özel kaynakları ve imza dosyaları bu depoya dahil edilmez.
