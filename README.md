# Portofolio SCSS — Tugas Rutin 4

Konversi CSS Dashboard/Portofolio ke SCSS dengan arsitektur **7-1 pattern**.

## Struktur SCSS (7-1 Pattern)

```
src/scss/
├── abstracts/     # variables, mixins, functions
├── base/          # reset, typography, global
├── components/    # buttons, cards, forms
├── layout/        # header, grid, footer
├── pages/         # home
├── themes/        # light, dark
├── vendors/       # placeholder vendor css
└── main.scss      # entry point (@use semua partial)
```

## Requirement yang Dipenuhi

- Konversi CSS existing ke SCSS (modular)
- Variables untuk colors & spacing (map `$colors`, `$spacings`)
- Nesting maksimal 3 level (`form > p > input`)
- 5 mixin reusable (`flex-center`, `responsive`, `transition`, `grid-area`, `surface`)
- Struktur 7-1 pattern
- Menggunakan `@use` (bukan `@import`)
- `@each` loop pada themes (`_light.scss`, `_dark.scss`)
- Dikompilasi dengan Dart SASS

## Menjalankan

```bash
npm install          # install dart-sass
npm run build:css    # produksi (minified)   -> style.css
npm run build:css:dev# pengembangan (expanded)
npm run watch:css    # auto-compile saat file berubah
```

Halaman `index.html` tetap memakai `style.css` (hasil kompilasi), jadi tidak perlu perubahan HTML.