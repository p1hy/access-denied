# NULL — ACCESS DENIED

A monochrome, terminal-inspired single-page GitHub Pages site. No backend, build step, or package manager required.

## Set your YouTube video

Open `index.html`, search for:

```js
const VIDEO_URL = 'https://www.youtube.com/watch?v=PFko4Kut39s';
```

Replace the demo trailer URL with your own YouTube video URL (normal link, short link or video ID).

You can also preview an alternate video by appending `?v=YOUR_VIDEO_ID` to your site's address.

**Autoplay behavior:** modern browsers usually only allow videos to autoplay muted. The video starts muted; visitors can press **ENABLE AUDIO** for sound. The video owner must allow external embeds for YouTube playback.

## GitHub Pages deployment

1. Create a public GitHub repository, e.g. `access-denied`.
2. Upload `index.html` and `favicon.svg` to the repository **root** (not a subfolder).
3. Go to **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Choose `main` and `/(root)`, then **Save**.
5. Your site will usually be available at `https://YOUR-USERNAME.github.io/access-denied/` after deployment completes.

For an address ending in a custom domain such as `access-denied.com`, you must own/configure that domain in Pages settings; the browser tab name is already `ACCESS DENIED — NULL`.

## Customize

Edit the text directly in `index.html`. It is all self-contained and uses no libraries other than the Google Fonts stylesheet and YouTube player API (both require a network connection).


## YouTube 153 hatası
YouTube, gömülü oynatıcı için geçerli bir HTTP Referer ister. `index.html` dosyasını doğrudan
çift tıklayıp `file://` olarak açtığınızda 153 hatası çıkabilir. GitHub Pages üzerinden
(`https://KULLANICI.github.io/access-denied/`) deneyin veya yerelde klasörde
`python -m http.server 8000` çalıştırıp `http://localhost:8000` açın.
Bu projede `strict-origin-when-cross-origin` referrer politikası açıkça tanımlıdır.
GitHub Pages üzerinde de hata varsa tarayıcı gizlilik/eklenti ayarlarını kontrol edin;
ayrıca videonun gömülmesine izin verildiğinden emin olun.
