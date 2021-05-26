# Under the Hood

The blog is setup using [Hugo](https://gohugo.io/) with the [Cupper](https://github.com/zwbetz-gh/cupper-hugo-theme) theme, and hosted on Github pages with a [custom domain](https://flutter.fyi)

---

## Setup Steps

Follow the [quickstart](https://gohugo.io/getting-started/quick-start/) guidance to setup Hugo, validate install, and create a default site (in folder "www/")

```
$ brew install hugo
$ hugo version
hugo v0.83.1+extended darwin/amd64 BuildDate=unknown
$ hugo new site www
```

Add a new theme in that directory. I'm using [cupper](https://github.com/zwbetz-gh/cupper-hugo-theme)

```
$ cd www
$ git submodule add https://github.com/zwbetz-gh/cupper-hugo-theme.git themes/cupper-hugo-theme
```

Test theme with example site to see what that looks like:

```
$ cd themes/cupper-hugo-theme/exampleSite
$ hugo server --themesDir ../..
```

Then configure/customize your site by removing default (config.toml) and replacing it with (config.yaml) from the example site.

```
$ cd www/
$ rm config.toml
$ cp themes/cupper-hugo-theme/exampleSite/config.yaml .
```

Create a couple of default posts:
```
$ hugo new post/hello-world.md
$ hugo new about.md
$ hugo new _index.md
```

Complete other config steps:
 * Update config.yaml metadata
 * Add favicon images
 * Add logo images
 * Update about, _index.md (Homepage)
 * Add preliminary tags
 
---

> TODO

 * Automate with GitHub Actions
 * Automate syndication to dev.to