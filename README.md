Source code for [danielle-li.github.io](https://danielle-li.github.io/)

Forked from [vikpe/github-pages-starter](https://github.com/vikpe/github-pages-starter). Thank you!

## Install

You should only have to do this once

1. Install system dependencies
  - If `which brew` returns no output, install [Homebrew](https://brew.sh/)
  - If `which nvm` returns no output
      - Install [nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
      - After installing, run `exec zsh` (to reload your terminal shell, which is zsh)
  - If `which node` returns no output
      - Then `nvm install 16`
      - Then `nvm use 16`
  - Install yarn: `npm install --global yarn`
  - Install `chruby`, `ruby-install` and install Ruby (see: https://mac.install.guide/ruby/12.html)
      - `brew install ruby-install chruby`
      - Follow directions to add lines to `~/.zshrc`
      - `ruby-install --latest`
      - Restart terminal
2. Clone repo: `git clone git@github.com:danielle-li/danielle-li.github.io.git`
3. Install system dependencies
  1. `cd danielle-li.github.io.git`
  2. `yarn install`
  3. `cd docs`
  4. `bundle install`

---

## Development

Run the following command from the root of the repo:

```shell
yarn watch
```

Site is served @ http://localhost:3000 (visit it in your browser)

---

## Production

Run the following command from the root of the repo:

```shell
yarn build
```

Build site to `/public`

---

Then, commit your changes and push them:

1. `git add -A`
2. `git commit -m <descriptive message of what you did>`
3. `git push origin master`

## Commands

Command | Stage | Description
---|---|---
`dev` | `dev` | Build site (Jekyll, assets)
`dev:jekyll` | `dev` | Build Jekyll
`dev:assets` | `dev` | Build assets (images, stylesheets)
`watch` | `dev` | Build site on changes and serve @ http://localhost:3000
||
`build` | `prod` | Build site (Jekyll, assets)
`build:jekyll` | `prod` | Build Jekyll
`build:assets` | `prod` | Build assets (images, stylesheets)
||
`clean` | - | Delete `/public` and clear Jekyll caches
`start` | - | Serve `/public` @ http://localhost:3000

## See also

* [Gatsby](https://github.com/gatsbyjs/gatsby) - Build blazing fast, modern apps and websites with React
* [Next.js](https://github.com/zeit/next.js) - React based framework with server side rendering (SSR)
