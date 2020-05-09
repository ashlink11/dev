# Version 4 Build Process from Dojo Project

I created the [dojo project](https://github.com/hashbangash/dojo) so I could build a toolchain from scratch to develop and build my portfolio. I followed the basic build process from the tutorial in the dojo project.

A few instructions were different, since the dojo project builds a React app and this is a Bootstrap web app.

Here are the steps I took:

`yarn init`

Followed the [Parcel Bootstrap Recipe](https://parceljs.org/recipes.html#bootstrap-+-fontawesome):
```
yarn add bootstrap jquery popper.js
yarn add --dev parcel-bundler
```
Add this to `package.json` for now:
```
  "scripts": {
    "start": "parcel index.html"
  }
```

Follow the [Parcel Sass docs](https://parceljs.org/scss.html):

`yarn add --dev sass`

Add this to my html `head`:

```html
<link rel="stylesheet" href="./index.scss">
```

Add this to my `index.js`:
```js
import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.css'
```

Add [Parcel CLI](https://github.com/parcel-bundler/parcel#parcel-cli):
`yarn add --dev parcel@next`

Test the dev environment with `yarn start`. Open <http://localhost:1234/>.

Test the production build with: `parcel build index.html`. Observe the output and file sizes.

***

Follow [React GitHub pages deployment tutorial](https://create-react-app.dev/docs/deployment/#github-pages).

`yarn add gh-pages`

Add to `package.json`:
```json
"homepage": "https://hashbangash.github.io/dev",
"scripts": {
  "start": "parcel serve index.html",
  "build": "parcel build index.html --public-url /dev/",
  "predeploy": "yarn build",
  "deploy": "gh-pages -d dist"
}

```

Merge code to master and:
`yarn deploy`

Success!
