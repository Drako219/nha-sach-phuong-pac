# Phương Pắc Bookstore

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![No JavaScript](https://img.shields.io/badge/JavaScript-none-lightgrey)
[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-0f5c4d?logo=github)](https://drako219.github.io/nha-sach-phuong-pac/)

A multi-page online bookstore website built with **pure HTML and CSS, no JavaScript**.
Final project for the *Basic Web Design* course at PTIT, made by a team of four. Each member builds ten pages, and each page has its own layout.

| | Link |
| --- | --- |
| Live site | https://drako219.github.io/nha-sach-phuong-pac/ |
| Figma design: all 41 pages, one row per member | [Open in Figma](https://www.figma.com/design/4ccWSWQ7MxSPAx8GqAavXD/?node-id=0-1) |
| Clickable prototype (11 core pages) | [Open in Figma Make](https://www.figma.com/make/0zNIPTh3nnnfM3zawh7ckN) |

In the Figma file, open the page **"Nhà sách – 41 trang"**. Frames are named `N<member>-<number> <Page> · <file>.html`, for example `N1-02 Khuyến mãi · khuyen-mai.html`. Frames marked ★ also have a clickable version in Figma Make.

## Highlights

- **No JavaScript.** Every interaction uses CSS only: `:checked`, `:target`, `<details>`, `:hover`, `:focus-within` and `:has()`.
- **Shared design tokens** for colour, type, radius and shadow in `css/bien.css`, so all 41 pages look like one site.
- **12-column grid** with a 1200px container, responsive at 1440, 768 and 375px.
- **Accessible markup** with landmarks, a breadcrumb, `aria-*` labels and visible focus states.

## Project structure

```text
.
├── _mau.html          Page template (header, navigation, footer). Copy it to start a new page
├── css/
│   ├── bien.css       Design tokens: colours, fonts, radius, shadows (shared)
│   ├── chung.css      Grid, buttons, form fields, book card, header, menu, footer (shared)
│   └── nguoi-X.css    Styles owned by member X (1–4), created by each member
├── img/               Images
├── fonts/             Local fonts
└── *.html             Pages (index.html is the home page)
```

## Team and pages

| Member | Area | Pages |
| --- | --- | --- |
| 1 | Showcase & marketing | `index` · `khuyen-mai` · `tu-sach-kinh-dien` · `sach-moi-theo-tuan` · `xep-hang` · `the-qua-tang` · `goi-qua` · `gioi-thieu` · `tuyen-dung` · `hoi-sach` |
| 2 | Products & discovery | `danh-muc` · `van-hoc` · `chi-tiet-sach` · `chi-tiet-vpp` · `combo` · `doc-thu` · `so-sanh` · `tac-gia` · `tac-gia-a-z` · `goi-y-sach` |
| 3 | Checkout & account | `gio-hang` · `thanh-toan` · `hoan-tat` · `tra-cuu-don` · `dang-nhap` · `quen-mat-khau` · `tai-khoan` · `don-hang` · `hoa-don` · `ho-so` |
| 4 | Content & support | `goc-doc-sach` · `bai-viet` · `cau-lac-bo` · `lich-su-kien` · `cua-hang` · `chi-tiet-cua-hang` · `tro-giup` · `chinh-sach` · `lien-he` · `so-do-trang` · `404` |

The Figma file shows the target design for every page above.

## Workflow

`main` is protected: nobody pushes to it directly, and every change goes through a pull request with one approval.

1. Sync: `git checkout main && git pull`
2. Branch: `git checkout -b feature/<page-name>`
3. Copy `_mau.html` to `<page-name>.html`. Update the `<title>`, link your `css/nguoi-X.css` (create it the first time), fix the breadcrumb, and add the class `dang-chon` to this page's menu item.
4. Commit and push: `git commit -m "<page-name>: short description"`, then `git push -u origin feature/<page-name>`
5. Open a pull request into `main` and ask one teammate to review. Merge once it is approved, then delete the branch.

To run the site locally, open `index.html` in a browser. There is no build step.

## Conventions

- Edit only your own pages and your own `css/nguoi-X.css`.
- `css/bien.css`, `css/chung.css` and `_mau.html` are shared. Tell the team first and change them on a `chung/<task>` branch.
- Class names are Vietnamese without diacritics, in kebab-case, for example `.the-sach` (book card) and `.menu-chinh` (main menu). Page content stays in Vietnamese.
- No JavaScript, no CSS frameworks. Every page must work at 1440, 768 and 375px before it is merged.

## License

Coursework for PTIT. All book titles and brand names are used for educational purposes only.
