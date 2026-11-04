# Arthyra Studio

Geliştirici tanıtım sayfası ve Güne Bir Söz gizlilik politikası.

Canlı site: https://arthyrastudio.info/ (eski `https://onrart.github.io/arthyra-studio/` adresleri buraya yönlenir)

Google Play gizlilik URL’si: https://arthyrastudio.info/gunebirsoz/gizlilik/ Statik HTML/CSS; üçüncü taraf yazı tipi, analitik veya JavaScript gerektirmez.

## Yerel geliştirme

1. `site.json` içindeki herkese açık destek e-postasını ayarlayın.
2. `python generate.py --publish` ile sayfaları üretin.
3. `python -m http.server 8787 --bind 127.0.0.1 --directory docs` ile önizleyin.

GitHub Pages yayın kaynağı: `main` dalı, `/docs` klasörü. Özel alan adı `docs/CNAME` dosyasındadır; silinirse site github.io adresine döner.

Türkçe politika: `/gunebirsoz/gizlilik/`; English: `/gunebirsoz/privacy/`.
