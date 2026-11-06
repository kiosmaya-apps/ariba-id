# ariba.id

Situs statis halaman depan ARIBA (aplikasi koperasi digital) untuk GitHub Pages.

- `index.html` — halaman depan (SEO: title, meta description, canonical, Open Graph, JSON-LD Organization/WebSite/SoftwareApplication/FAQPage)
- `fitur/` — halaman Fitur (SEO: "fitur aplikasi koperasi digital"), termasuk dompet anggota
- `skor-kredit/` — ketentuan Skor Kredit Ariba Indonesia (ARIBA-SKOR-2.0)
- `demo/` — prototipe ARIBA Cooperative OS dengan data contoh (noindex)
- `img/` — screenshot aplikasi (data contoh), `og/` — gambar pratinjau tautan
- `robots.txt`, `sitemap.xml`, `404.html`

## Memasang

Situs ariba.id berjalan di hosting DirectAdmin (`public_html`). Setiap push ke `main` diunggah otomatis oleh GitHub Actions (`.github/workflows/deploy.yml`) lewat FTPS. DNS tidak perlu diubah.

Aplikasi lain di hosting yang sama (Kasbon, Jembara, dll.) aman: workflow hanya mengunggah file dari repositori ini dan hanya menghapus file yang dulu ia unggah sendiri (dicatat di `.ftp-deploy-sync-state.json` di server). Tidak ada `.htaccess` di akar.

Pengaturan sekali saja (Settings → Secrets and variables → Actions):

| Jenis | Nama | Isi |
|---|---|---|
| Secret | `FTP_SERVER` | mis. `ftp.ariba.id` atau IP server |
| Secret | `FTP_USERNAME` | akun FTP |
| Secret | `FTP_PASSWORD` | kata sandi akun FTP |
| Variable (opsional) | `FTP_DIR` | bawaan `public_html/` untuk akun `deploy@ariba.id` (path `/home/attaqwac/domains/ariba.id/`); `domains/ariba.id/public_html/` bila memakai akun utama |
| Variable (opsional) | `FTP_PROTOCOL` | `ftps` (bawaan) atau `ftp` |

Akun yang dipakai: `deploy@ariba.id` (sudah ada di DirectAdmin → FTP Management).

Setelah tayang, daftarkan `https://ariba.id/sitemap.xml` di Google Search Console.
