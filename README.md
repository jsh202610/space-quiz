# Space Exploration Quiz

A lightweight, responsive quiz about space exploration, planets, and historic
missions. Answer ten questions in a randomized order, get immediate feedback,
track your score, and play again. Choose answers with the mouse or the `1`-`4`
and `A`-`D` keys. The interface supports light and dark color schemes and reduced
motion preferences.

The app is a standalone `index.html` containing HTML, CSS, and JavaScript. No
package installation or build step is needed.

## Run locally

Open `index.html` directly in a browser, or use Python 3 to serve the repository:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Visit <http://127.0.0.1:8000/>. Stop the server with `Ctrl+C`.

## Browser tests

With the local server running, open
<http://127.0.0.1:8000/tests/quiz.test.html>. The page reports `PASS` or `FAIL` for
checks covering question shuffling, mouse and keyboard answers, scoring,
progress, and replay behavior.

## GitHub Pages

Site URL: <https://jsh202610.github.io/space-quiz/>

In the repository's **Settings > Pages**, select **GitHub Actions** as the
deployment source. The workflow in `.github/workflows/pages.yml` runs the browser
tests on pull requests targeting `main` and on pushes to `main`. After successful
tests on `main`, it uploads and deploys only `index.html` and a `.nojekyll` marker.
There are no build dependencies or generated application bundles.

To redeploy manually, run **Test and deploy GitHub Pages** from the **Actions**
tab with the `main` branch selected. Other branches can run the tests manually
but cannot deploy. Deployment status and the published URL are available in the
workflow's `github-pages` environment.
