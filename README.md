# ariba.id

Situs statis halaman depan ARIBA (aplikasi koperasi digital) untuk GitHub Pages.

- `index.html` — halaman depan (SEO: title, meta description, canonical, Open Graph, JSON-LD Organization/WebSite/SoftwareApplication/FAQPage)
- `skor-kredit/` — ketentuan Skor Kredit Ariba Indonesia (ARIBA-SKOR-2.0)
- `demo/` — prototipe ARIBA Cooperative OS dengan data contoh (noindex)
- `img/` — screenshot aplikasi (data contoh), `og/` — gambar pratinjau tautan
- `CNAME` — domain kustom `ariba.id`; `robots.txt`, `sitemap.xml`, `404.html`

## Memasang

1. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
2. DNS domain ariba.id:
   - Record `A` untuk `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - Record `CNAME` untuk `www`: `<akun-atau-organisasi>.github.io`
3. Setelah DNS aktif, centang *Enforce HTTPS*.
4. Daftarkan `https://ariba.id/sitemap.xml` di Google Search Console.
