# MaksForge pages theme

The Jekyll theme for the MaksForge app sites at `maksforge.com/<app>/`. It matches the home page at [maksforge.com](https://maksforge.com) and loads that site's `/assets/style.css`, so a project site only renders correctly when it's served from maksforge.com.

To use it, an app's `docs/_config.yml` needs:

```yaml
remote_theme: maks-sredniawa/pages-theme
plugins:
  - jekyll-remote-theme
maksforge:
  icon: /assets/icons/<app>.webp
  status: live        # live, building or oss
  play: https://play.google.com/store/apps/details?id=<package>   # optional
  chrome: https://chromewebstore.google.com/detail/<slug>/<id>   # optional
  facts:                # optional, extra rows in the fact list on the app's home page, alongside the Status, Price, Package, Source and Privacy rows the layout adds itself
    - label: Requires
      value: Android 8.0+
      mono: true
```

`title` and `description` in the same file fill the app header. The page's `##` headings become its numbered contents list. Every class the layout uses (`mf-*`) is styled by the shared stylesheet; `assets/css/app.css` only adapts it to Jekyll's output. The maksforge.com deploy (`maks-sredniawa/maks-sredniawa.github.io`) fetches the theme on every build and checks for changes every 15 minutes, so a change here reaches every app within about 15 minutes.
