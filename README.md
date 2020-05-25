# Hugo Learn Theme

This repository contains a theme for [Hugo](https://gohugo.io/), based on the great [Learn](https://github.com/matcornic/hugo-theme-learn/) theme.

## Installation

Create a hugo site following their [quick start tutorial](https://gohugo.io/getting-started/quick-start/).

Run the following to bring in this theme.

```shell
echo 'theme = "workerpedia"' >> config.toml
echo '/public' >> .gitignore
cd themes/
git clone https://github.com/the-idc/hugo-theme-workerpedia.git workerpedia
```

## Customize

Add your logo to `static/logo.png`

Run the following to add settings to the bottom of `config.toml` then set the other variables like title.

```
cat << EOF >> config.toml
[params]
disableNextPrev = true
themeVariant = "red"
custom_css = [ "custom.css" ]

[outputs]
home = [ "HTML", "RSS", "JSON"]

[permalinks]
top = "/:filename/"
EOF
```

Add some information to your front page by creating a file at `content/_index.md`

## Add claims

`hugo new claims/what-have-unions-done-for-me.md`

Fill in the blanks, categories are displayed on the left sidebar of the page.

## Test

```
hugo serve
```

## Add to github
In github, create a new repository. (make sure to fill in `<user>` and `<repo>` below.

```
git init
git commit -am "First commit"
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin master
```

## Hosting

Get a [netlify](https://netlify.com) account, add the github repo as a new site, rename and share the url.

## Need help?

Raise an issue on the [theme repo](https://github.com/the-idc/hugo-theme-workerpedia/issues) and we'll make sure to get you started.
