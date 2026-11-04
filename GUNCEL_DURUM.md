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
- Sınır: Bu makinenin DNS önbelleği hâlâ eski Squarespace adresini veriyordu; tarayıcı park sayfasını ("Yakında") gösterdi. Sitenin yeni alan adında GitHub içeriğini sunduğu bu makineden henüz görülmedi. Eski kayıtların TTL'si 1–4 saat; bu sürede eski önbellekli ziyaretçiler de park sayfasını görebilir. Bu makineden komut satırı DNS sorgusu yapılamadı (dış DNS'e erişim kapalı).

## Açık işler

- Önbellek dolunca (4 Kasım akşamı) üç adresin GitHub içeriğini döndürdüğünü tarayıcıda doğrula.
- Google Play Console → Uygulama içeriği → Gizlilik politikası URL'sini `https://arthyrastudio.info/gunebirsoz/gizlilik/` yap (eski adres yönlendirdiği için acil değil).
- Mobil uygulamada politika bağlantısının Ayarlar'a eklenmesi; uygulamanın güncel durum dosyasında takip edilir.
- DMARC birkaç hafta rapor topladıktan sonra `p=quarantine` düşünülebilir.

Doğrulama (ilk yayın): Üç HTML sayfasında etiket dengesi, tek h1, benzersiz kimlikler, yerel bağlantı/varlıklar, doğru iletişim adresi ve script bulunmadığı doğrulandı; üç public HTTPS adresi github.io üzerinde HTTP200 döndü.

Politika dayanağı: Güne Bir Söz 1.1.1 uygulamasının storage, catalog, wikiquote, notifications, widget, story ve Android manifesti statik incelemesi. Yerel kayıt, doğrudan Vikisöz bağlantısında ağ metadatası, yerel bildirim, kullanıcı başlatmalı paylaşım ve allowBackup=true sistem yedeklemesi açıklanır. Google kabulü/hukuki uygunluk garantisi verilmez.

Yayın kapsamı bu site dosyaları ve kamuya açık logolardır. Mobil uygulamanın özel kaynakları ve imza dosyaları bu depoya dahil edilmedi. site.json ve generate.py, sonraki politika/iletişim güncellemeleri için tek kaynaktır; `python generate.py --publish` sonrası HTML değişiklikleri commit/push ile Pages'e gider. Sayfalar göreli bağlantı kullanır; `base_url` şu an üreteçte kullanılmıyor.
