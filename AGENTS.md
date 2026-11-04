# Arthyra Studio — geliştirici ve gizlilik sitesi

GitHub Pages için buildless HTML/CSS sitesi. Yayıncı Arthyra Studio; ilk uygulama Güne Bir Söz. Mobil uygulama kaynakları bu depoya kopyalanmaz.

- `site.json`: genel site adresi, kullanıcı tarafından seçilecek herkese açık destek e-postası, politika tarihi.
- `generate.py`: ana sayfa ve TR/EN gizlilik HTML'lerini üretir.
- `docs/`: GitHub Pages yayın kökü; CSS ve yerel marka görselleri burada.
- `docs/GUNCEL_DURUM.md`: güncel durum ve sonraki adım.

Komutlar: `python generate.py` yerel taslak üretir; `python generate.py --publish` iletişim e-postası eksikse durur. `python -m http.server 8787 --bind 127.0.0.1 --directory docs` yerel önizleme.

Gizlilik metni gerçek uygulama koduyla tutarlı tutulmalı. Yeni analitik/reklam, veri aktarımı, hesap veya hizmet eklenirse metni güncelle. Cihaz yedeklemesini yokmuş gibi anlatma: uygulamada Android allowBackup=true. İletişim adresini kullanıcı seçmeden yayınlama. GitHub Pages hedefi `onrart/arthyra-studio`, dal main, kaynak /docs. Diğer projelerin özel kaynakları ve imza dosyaları bu depoya dahil edilmez.
