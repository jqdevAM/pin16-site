# pin16-site

The public pages for the Pin16 Android app.

| Page | URL |
|---|---|
| Privacy policy | https://jqdevAM.github.io/pin16-site/privacy/ |
| Fault codes, English | https://jqdevAM.github.io/pin16-site/codes/ |
| Fault codes, Russian | https://jqdevAM.github.io/pin16-site/ru/codes/ |

Published with GitHub Pages: Settings → Pages → Deploy from a branch →
`main`, folder `/` (root).

The page is the copy kept in the app's own repository, at
`site/privacy/index.html`. **Change it there and copy it here**, so the
policy and the behaviour it describes stay together — every sentence in it is
a claim about what the app stores, what leaves the device, and what it asks
the phone for.

## The fault-code pages

`codes/`, `ru/codes/`, `assets/codes.css` and `sitemap.xml` are **generated**,
by `tool/site/build_code_pages.py` in the app's repository, from the same
database the app ships. Do not edit them here: the next run replaces those
directories whole.

```bash
# in the pin16 repository, with this checkout next to it
python3 tool/dataset_bootstrap/build_dataset.py
python3 tool/site/build_code_pages.py      # writes into ../pin16-site
```
