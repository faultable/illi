# illi

Tema Ghost yang digunakan di blog [faultable.dev](https://faultable.dev) berdasarkan
tema [TryGhost/Starter](https://github.com/TryGhost/Starter) yang berfokus di pengalaman membaca.

<div align="center">

  <img src="https://i.imgur.com/ibsIMrh.png" alt="Halaman Beranda">

  <p>Halaman Beranda</p>

  <br>

  <img src="https://i.imgur.com/VG0Vj3L.png" alt="Lighthouse score">

  <p>Skor Lighthouse v1.0.0</p>

</div>

## Catatan

Ada beberapa "custom partials" disini, yakni:

- Font menggunakan PT Serif (400), IBM Plex Serif (400, 700i) yang di self-host
- `cta.hbs` - Ini buat yang kolom "Dukung" dibawah post
- `sidebar.hbs` - Ini yang ada disamping daftar post di halaman beranda

Jadi, silahkan ganti dengan kebutuhan kamu.

Btw, disini masih menggunakan `className` yg acak-acakan, harap maklum. Tapi gak usah khawatir, nama hanyalah nama.

## Konfigurasi

- Ganti `img/profile.jpg` dengan gambar kamu. Pakai ekstensi `jpg` karena _default_ nya dari GitHub gitu.
- Ganti konten yang ada di `partials/cta.hbs` dan `partials/sidebar.hbs`
- Jika kamu memiliki forum Discourse, silahkan di _uncomment_ bagian komentar di `post.hbs`

## Roadmap

yes.

---

# First time using a Ghost theme?

Ghost uses a simple templating language called [Handlebars](http://handlebarsjs.com/) for its themes.

We've documented our default theme pretty heavily so that it should be fairly easy to work out what's going on just by reading the code and the comments. Once you feel comfortable with how everything works, we also have full [theme API documentation](https://themes.ghost.org) which explains every possible Handlebars helper and template.

**The main files are:**

- `default.hbs` - The main template file
- `index.hbs` - Used for the home page
- `post.hbs` - Used for individual posts
- `page.hbs` - Used for individual pages
- `tag.hbs` - Used for tag archives
- `author.hbs` - Used for author archives

One neat trick is that you can also create custom one-off templates just by adding the slug of a page to a template file. For example:

- `page-about.hbs` - Custom template for the `/about/` page
- `tag-news.hbs` - Custom template for `/tag/news/` archive
- `author-ali.hbs` - Custom template for `/author/ali/` archive

# Development

Styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# Install
yarn

# Run build & watch for changes
$ yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/<theme-name>.zip`, which you can then upload to your site.

```bash
yarn zip
```

# PostCSS Features Used

- Autoprefixer - Don't worry about writing browser prefixes of any kind, it's all done automatically with support for the latest 2 major versions of every browser.
- Variables - Simple pure CSS variables
- [Color Function](https://github.com/postcss/postcss-color-function)

# License

[MIT](LICENSE)
