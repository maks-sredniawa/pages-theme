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
```

`title` and `description` in the same file fill the app bar. GitHub Pages fetches the theme on every build of the app site, so a change here reaches an app the next time its site rebuilds.
