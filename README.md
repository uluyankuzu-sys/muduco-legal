# Muduco — yasal sayfalar

Gizlilik politikası ve kullanım koşulları. Google Play, gizlilik politikası için
**herkese açık bir URL** zorunlu tutuyor; kendi alan adında olması şart değil.

## Dosyalar

| dosya | içerik |
|---|---|
| `index.html` | İki dilli giriş sayfası + hesap silme talimatı |
| `gizlilik.html` / `privacy.html` | Gizlilik politikası (TR / EN) |
| `kullanim-kosullari.html` / `terms.html` | Kullanım koşulları (TR / EN) |
| `style.css` | Ortak stil (açık/koyu tema destekli) |

## GitHub Pages ile yayınlama (ücretsiz, ~10 dakika)

1. GitHub'da **`muduco-legal`** adında yeni ve **herkese açık (public)** bir depo aç.
2. Bu klasördeki dosyaları o deponun köküne yükle
   (sürükle-bırak da olur: *Add file → Upload files*).
3. Depoda **Settings → Pages** → *Source*: `Deploy from a branch`,
   *Branch*: `main` / `/ (root)` → **Save**.
4. 1-2 dakika sonra adres hazır olur:
   `https://uluyankuzu-sys.github.io/muduco-legal/`

## Sonra mutlaka yap

- Adresi tarayıcıda aç ve gerçekten açıldığını gör. **Ölü bir gizlilik
  politikası bağlantısı, Play incelemesinde reddedilme sebebidir.**
- Adres değişirse
  [`src/data/legal-urls.ts`](../src/data/legal-urls.ts) içindeki `BASE`
  sabitini güncelle — uygulamadaki bağlantılar oradan okunuyor.
- Play Console'da **Uygulama içeriği → Gizlilik Politikası** alanına
  `.../gizlilik.html` adresini gir.

## Kendi alan adını bağlamak (isteğe bağlı)

`muduco.com` alırsan GitHub Pages'e özel alan adı olarak bağlayabilirsin
(Settings → Pages → *Custom domain*). Hosting ücretsiz kalır, yalnızca alan
adının yıllık ücretini ödersin. Bağladıktan sonra `legal-urls.ts`'teki `BASE`'i
`https://muduco.com/legal` gibi yeni adresle güncelle.

> Not: Uygulamanın adı **Muduco** ve paket adı `com.muduco.app`.
> Alan adını alırken harf sırasına dikkat et — `mudico` değil, **`muduco`**.

## Metni güncellemek

Metinler uygulamanın bugünkü davranışına göre yazıldı ve şu iddiaları içeriyor:

- ağ istekleri yalnızca: Firebase (hesap), Sentry (çökme kaydı), seçilen giriş
  hizmeti (Google / Apple) ve El Akoru oyununun MediaPipe indirmesi
  (cdn.jsdelivr.net, storage.googleapis.com); analitik/telemetri yok, reklam yok
- mikrofon sesi ve kamera görüntüsü cihazdan çıkmıyor, kaydedilmiyor
- bazı sesler açık lisanslı üçüncü taraf kayıtlardan (uygulamada Ayarlar →
  Teşekkürler; kaynak listesi uygulama deposunda `assets/sounds/LISANSLAR.md`)

**Bu davranışlardan biri değişirse metni de güncelle.** Örneğin Sentry (çökme
raporlama) eklenirse "analitik veya çökme raporlama aracı kullanmıyoruz"
cümlesi doğru olmaktan çıkar.
