# KDP SYSTEM — GitHub Portal

Portal satu alamat untuk membuka:

- **KDP Mart** — aplikasi produksi
- **KDP Scanner** — aplikasi pendataan barang baru

Tampilannya dibuat mengikuti mockup KDP System: header hijau, dua kartu aplikasi, dan tiga kartu informasi.

## 1. Isi URL aplikasi

Buka file `config.js` lalu ubah:

```js
kdpMartUrl: "PASTE_KDP_MART_URL_HERE",
kdpScannerUrl: "PASTE_KDP_SCANNER_URL_HERE",
```

Contoh:

```js
window.KDP_PORTAL_CONFIG = {
  kdpMartUrl: "https://script.google.com/macros/s/AKfycbXXXX/exec",
  kdpScannerUrl: "https://script.google.com/macros/s/AKfycbYYYY/exec",
  openInNewTab: true
};
```

Tidak perlu mengubah Google Apps Script hanya untuk portal ini, karena tombol membuka masing-masing Web App secara langsung.

## 2. Upload ke GitHub

Buat repository, misalnya:

`kdp`

Upload semua file ini ke root repository:

- `index.html`
- `styles.css`
- `config.js`
- `.nojekyll`
- `README.md`

## 3. Aktifkan GitHub Pages

Repository GitHub → **Settings** → **Pages**

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/(root)`
- Save

Alamat portal nantinya:

`https://USERNAME.github.io/kdp/`

## Struktur sistem

```text
GitHub Portal KDP
        |
        |-- KDP Mart ------> Web App GAS produksi ------> Spreadsheet KDP Mart
        |
        `-- KDP Scanner ---> Web App GAS scanner -------> Spreadsheet master baru
```

Portal hanya menjadi pintu masuk. Database kedua aplikasi tetap terpisah.

## Custom domain

Jika nanti ingin lebih pendek dan profesional, GitHub Pages bisa diberi domain sendiri, misalnya:

- `kdp.domainanda.com`
- `app.domainanda.com`

Atur melalui **Settings → Pages → Custom domain**.
