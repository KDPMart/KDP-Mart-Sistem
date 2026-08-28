# KDP SYSTEM GITHUB PORTAL V2

Versi ini membuat URL GitHub tetap terlihat saat KDP Mart / KDP Scanner dibuka.

## Sebelum upload ke GitHub

Pastikan pada `doGet()` kedua aplikasi Google Apps Script sudah ditambahkan:

```javascript
.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL);
```

Lalu deploy ulang masing-masing GAS sebagai **New version**.

## Isi config.js

```js
window.KDP_PORTAL_CONFIG = {
  kdpMartUrl: "https://script.google.com/macros/s/.../exec",
  kdpScannerUrl: "https://script.google.com/macros/s/.../exec"
};
```

## Upload ke GitHub

Upload semua file ini ke root repository:

- index.html
- mart.html
- scanner.html
- styles.css
- config.js
- .nojekyll

Aktifkan GitHub Pages:

Settings > Pages > Deploy from a branch > main > /(root)

## Hasil URL

Portal:
`https://USERNAME.github.io/kdp/`

KDP Mart:
`https://USERNAME.github.io/kdp/mart.html`

KDP Scanner:
`https://USERNAME.github.io/kdp/scanner.html`

Address bar tetap GitHub. Google Apps Script tampil di iframe.
