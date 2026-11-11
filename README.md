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
  kind: Android app   # optional, the label under the name; otherwise it comes from play or chrome
```

Each page opens with the app's row from the maksforge.com home list: icon, `title`, kind, the store and source links, the package and the status. On the app's home page the text before the first `##` heading sits in that row; other pages show `description` there and start with their own text. "← All apps" goes back to the app's row on the home page, which is found by the icon's file name. Pages longer than 500 words get an "On this page" list of their `##` headings. Every class the layout uses (`mf-*`, plus the home page's `topbar`, `wordmark` and `about` pair) is styled by the shared stylesheet; `assets/css/app.css` only adapts it to Jekyll's output. The maksforge.com deploy (`maks-sredniawa/maks-sredniawa.github.io`) fetches the theme on every build and checks for changes every 15 minutes, so a change here reaches every app within about 15 minutes.
