<p align="center">
  <a href="https://github.com/Spenhouet/jekyll-4-gh-pages-quickstart/actions/workflows/github-pages.yml"><img src="https://github.com/Spenhouet/jekyll-4-gh-pages-quickstart/actions/workflows/github-pages.yml/badge.svg" alt="Build Status"></a><a href="https://github.com/Spenhouet/jekyll-4-gh-pages-quickstart/actions/workflows/pages/pages-build-deployment"><img src="https://github.com/Spenhouet/jekyll-4-gh-pages-quickstart/actions/workflows/pages/pages-build-deployment/badge.svg" alt="Deploy Status"></a>
</p>

<p align="center">Template for Jekyll 4 with GitHub pages.</p>

<p align="center"><em>Check the result of this basic version out at <a href="https://spenhouet.com/jekyll-4-gh-pages-quickstart/">spenhouet.com/jekyll-4-gh-pages-quickstart</a>.</em></p>

This is a working version of this [guide](https://jekyllrb.com/docs/continuous-integration/github-actions/) using [helaili/jekyll-action](https://github.com/marketplace/actions/jekyll-actions) for the GitHub actions to deploy a Jekyll 4 page.

## Activate Deployment

In your repositories GitHub settings, go to `Pages` and set the source branch to `gh-pages` and `/ (root)`.
The GitHub action will build the Jekyll page and commit it to the `gh-pages` branch. The GitHub build in deployment action will then deploy the page.

## Local Development

For local development, Jekyll can be run in server mode inside the container. It will watch for changes, rebuild the site, and provide access through its included web server. You can then check the results of changes by reloading http://localhost:4000/ in a browser.

```bash
docker run --rm --volume="$PWD:/srv/jekyll:Z" -p 4000:4000 jekyll/jekyll:4.2.2 jekyll serve
```

If you provide a ``Gemfile`` and would like to update your ``Gemfile.lock`` you can run

```bash
docker run --rm --volume="$PWD:/srv/jekyll:Z" -it jekyll/jekyll:4.2.2 bundle update
```

## License

This template is released under the [MIT License](LICENSE).