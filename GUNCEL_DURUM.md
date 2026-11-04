# Güncel durum

4 Kasım 2026 — Yayında. Public depo: https://github.com/onrart/arthyra-studio ; GitHub Pages main:/docs, özel alan adı `arthyrastudio.info` (`docs/CNAME`).

- Ana sayfa: https://arthyrastudio.info/
- Türkçe gizlilik: https://arthyrastudio.info/gunebirsoz/gizlilik/
- English privacy: https://arthyrastudio.info/gunebirsoz/privacy/
- Eski `https://onrart.github.io/arthyra-studio/...` adresleri GitHub tarafından yeni alan adına yönlendirilir (GitHub Pages davranışı; yönlendirme ayrıca test edilmedi).
- Kullanıcının onayladığı iletişim adresi: destek@arthyrastudio.info.

## Alan adı bağlantısı (4 Kasım 2026)

- Squarespace DNS (kayıtlar Squarespace panelinde okunarak doğrulandı):
  - Squarespace varsayılan kayıt grubu (park sayfası A/CNAME/HTTPS) kullanıcı tarafından silindi.
  - Eklenenler: 4 A (`185.199.108-111.153`), 4 AAAA (`2606:50c0:8000-8003::153`), `www` CNAME `onrart.github.io`, `_github-pages-challenge-onrart` TXT, `_dmarc` TXT `v=DMARC1; p=none; rua=mailto:destek@arthyrastudio.info`.
  - Google Workspace MX/SPF/DKIM kayıtlarına dokunulmadı. Değişiklik öncesi kayıt dökümü oturum geçici klasöründe tutuldu, depoya alınmadı.
- GitHub hesap ayarlarında `arthyrastudio.info` "Verified" (Pages verified domain; alan adı ele geçirme koruması).
- Depo Settings → Pages: "DNS check successful", sertifika verildi, "Enforce HTTPS" açık (sayfa yenilenerek doğrulandı); GitHub "Your site is live at https://arthyrastudio.info/" gösteriyor.
- `https://onrart.github.io/arthyra-studio/gunebirsoz/gizlilik/` → `https://arthyrastudio.info/gunebirsoz/gizlilik/` yönlendirmesi tarayıcıda görüldü.
- Canlı doğrulama (curl, 4 Kasım 2026): `arthyrastudio.info` 185.199.x.153'e çözülüyor; `/`, `/gunebirsoz/gizlilik/`, `/gunebirsoz/privacy/` HTTPS 200 ve doğru başlıklar; gizlilik sayfasında `mailto:destek@arthyrastudio.info`; `http://` → 301; eski `/GUNCEL_DURUM.md` 404.
- Sınır: O anda `www.arthyrastudio.info` hâlâ önbellekteki Squarespace adresine (198.185.159.144) gidiyordu. Uygulama içi tarayıcı paneli de kendi önbelleğiyle park sayfasını ("Yakında") gösteriyordu. Eski kayıtların TTL'si 1–4 saat.
- Google Play Console → Uygulama içeriği → Gizlilik politikası URL'si `https://arthyrastudio.info/gunebirsoz/gizlilik/` olarak kaydedildi (önceki: github.io adresi). Kullanıcı onayıyla 4 Kasım 2026'da incelemeye gönderildi; yayın özetinde "İncelenmekte olan değişiklikler" altında, önce otomatik hızlı kontroller (≤14 dk). Yönetilen yayınlama kapalı, onaylanınca kendiliğinden yürürlüğe girer.

## Teknik SEO (4 Kasım 2026)

- Üretece canonical, TR/EN hreflang (x-default TR), Open Graph/Twitter kartı, 1200×630 `og-image.jpg`, `sitemap.xml`, robots Sitemap satırı ve markalı `404.html` (noindex) eklendi.
- Doğrulama: dört HTML'de etiket dengesi, tek h1, benzersiz kimlik ve baş etiketleri Python HTMLParser ile; sitemap XML ayrıştırıldı; yerel önizlemede 404 masaüstü/mobil (375 px, yatay taşma yok) ve ana sayfa görselleri/konsol hatasız. Canlı (curl, push sonrası): `/`, gizlilik, `sitemap.xml`, `robots.txt`, `og-image.jpg` 200 ve doğru içerik türü; ana sayfada canonical ve og:image mutlak adresle; olmayan yol 404 ve markalı başlık. Paylaşım önizlemesi bir sosyal uygulamada denenmedi.

## Söz kataloğu (4 Kasım 2026)

- `docs/gunebirsoz/sozler-v1.json` canlı: HTTP 200, `application/json`, gzip ~161 KB, CORS `*`, 1.910 kayıt (curl ile doğrulandı). Üretim ve yazar seçimi gunluk-alinti deposunda (`scripts/`).
- Gizlilik TR/EN güncellendi: 1.1.2 kataloğu bu siteden (GitHub Pages) indirir, 1.1.1 Vikisöz API'sine bağlanır; kuruluma özgü sıra bilgisi cihazdan çıkmaz.

## Açık işler

- Play Console'da gizlilik URL incelemesinin onaylandığını kontrol et (Google: genelde 7 güne kadar).
- `www.arthyrastudio.info`'nun GitHub'a yönlendiğini önbellek dolunca doğrula.
- Mobil uygulamada politika bağlantısının Ayarlar'a eklenmesi; uygulamanın güncel durum dosyasında takip edilir.
- DMARC birkaç hafta rapor topladıktan sonra `p=quarantine` düşünülebilir.

Doğrulama (ilk yayın): Üç HTML sayfasında etiket dengesi, tek h1, benzersiz kimlikler, yerel bağlantı/varlıklar, doğru iletişim adresi ve script bulunmadığı doğrulandı; üç public HTTPS adresi github.io üzerinde HTTP200 döndü.

Politika dayanağı: Güne Bir Söz 1.1.1 uygulamasının storage, catalog, wikiquote, notifications, widget, story ve Android manifesti statik incelemesi. Yerel kayıt, doğrudan Vikisöz bağlantısında ağ metadatası, yerel bildirim, kullanıcı başlatmalı paylaşım ve allowBackup=true sistem yedeklemesi açıklanır. Google kabulü/hukuki uygunluk garantisi verilmez.

Yayın kapsamı bu site dosyaları ve kamuya açık logolardır. Mobil uygulamanın özel kaynakları ve imza dosyaları bu depoya dahil edilmedi. site.json ve generate.py, sonraki politika/iletişim güncellemeleri için tek kaynaktır; `python generate.py --publish` sonrası HTML değişiklikleri commit/push ile Pages'e gider. Sayfalar göreli bağlantı kullanır; `base_url` şu an üreteçte kullanılmıyor.
