# w0brc.github.io

Please visit the [W0BRC Boonville Amateur Radio Club website](https://w0brc.github.io).

## Running locally

You need Ruby and gem before starting, then:

```bash
# install bundler
gem install bundler

# clone the project
git clone https://github.com/w0brc/w0brc.github.io.git
cd w0brc.github.io

# install dependencies with bundler
bundle install

# run jekyll with dependencies
bundle exec jekyll serve
```

## Docker

Alternatively, you can deploy it using the multi-stage [Dockerfile](Dockerfile)
that serves files from Nginx for better performance in production.

Build the image for your site's `JEKYLL_BASEURL`:

```
docker build --build-arg JEKYLL_BASEURL="/your-base/url" -t w0brc.github.io .
```

(or leave it empty for root: `JEKYLL_BASEURL=""`) and serve it:

```
docker run -p 8080:80 w0brc.github.io
```

## License

Released under [the MIT license](LICENSE).
