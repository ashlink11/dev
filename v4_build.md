# Version 4 Build Process from Dojo Project

I created the [dojo project](https://github.com/hashbangash/dojo) so I could build a toolchain from scratch to develop and build my portfolio. I followed the basic build process from the tutorial in the dojo project.

A few instructions were different, since the dojo project builds a React app and this is a Bootstrap web app.

Here are the moves I made in:

`yarn init`

Followed the [Parcel Bootstrap Recipe](https://parceljs.org/recipes.html#bootstrap-+-fontawesome):
```
yarn add bootstrap jquery popper.js
yarn add --dev parcel-bundler
```
Add this to `package.json`:
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

Test the build. `parcel build index.html`. Observe the output and file sizes:

```
✨  Built in 10.27s.

dist/hashbangash.github.io.03d5d3e0.css.map                    265.76 KB     34ms
dist/manuel-meurisse-RlXU6DiifBg-unsplash.e765cf31.jpg         232.66 KB    4.74s
dist/forgiveness.0f49d7b2.png                                  223.44 KB    4.74s
dist/ruby.65b67b51.png                                         191.99 KB    4.74s
dist/styledcomponents.4874d398.png                             186.48 KB    4.74s
dist/Raleway-Regular.8b93386e.ttf                              168.94 KB    259ms
dist/Raleway-ExtraBold.65a97a69.ttf                            168.66 KB    259ms
dist/sarah-ball-WJHYGJWiOIU-unsplash.88698bb0.jpg               149.9 KB    4.70s
dist/hashbangash.github.io.03d5d3e0.css                        142.35 KB    8.00s
dist/ash_grevelink_boston__harbor_january_2020.077f1337.jpg    142.14 KB    4.69s
dist/postgres.fb64ba03.png                                     120.18 KB    4.73s
dist/cristina-gottardi-Bj7Pt0ZMBOk-unsplash.ad78bb5e.jpg       108.48 KB    4.69s
dist/pollaris.3e47b5e3.png                                      99.77 KB    4.69s
dist/grunt.698d8fc0.png                                         94.86 KB    4.73s
dist/rails.6109d3cf.png                                          82.9 KB    4.65s
dist/ajax.fc364755.png                                          73.98 KB    4.65s
dist/heroku2.e75a0a5a.png                                       71.28 KB    4.65s
dist/CourierPrime-Regular.9e607886.ttf                          66.53 KB    215ms
dist/aws_s3.82affa0c.png                                        60.17 KB    4.64s
dist/kali9.5ac73169.png                                         53.76 KB    4.64s
dist/public/resume-2020-april-ash-grevelink.pdf                 46.63 KB    4.64s
dist/spring.3bf2c423.png                                        43.53 KB    4.64s
dist/mysql2.d67a851f.png                                        40.46 KB    4.64s
dist/react.22c0cb69.png                                         38.49 KB    4.63s
dist/c.918b9eb5.png                                             36.38 KB    4.63s
dist/mongodb.7c391871.png                                       35.83 KB    4.64s
dist/github3.1f6cecc3.png                                       31.83 KB    4.64s
dist/simple_fundamentals.811f7cdb.png                           31.18 KB    4.63s
dist/tictactoe.8c1d6f6b.png                                     26.21 KB    4.63s
dist/handlebars.c117d980.png                                    25.34 KB    4.63s
dist/docker.5dd62cea.png                                        22.23 KB    4.64s
dist/sass.a95bcfc1.png                                          21.18 KB    4.59s
dist/index.html                                                 20.32 KB    1.90s
dist/webpack.59af462f.png                                       17.42 KB    4.59s
dist/gcp.2ce30e70.png                                              17 KB    4.64s
dist/terminal.edb44591.png                                      13.04 KB    4.59s
dist/css3.ad77bf89.png                                          12.83 KB    4.59s
dist/angular.42b320c1.png                                       11.46 KB    4.59s
dist/bootstrap.c2e31b0f.png                                     11.28 KB    4.59s
dist/wordpress.d0648b45.png                                     11.04 KB    4.59s
dist/html2.c5964dc8.png                                         10.62 KB    4.59s
dist/java2.caa83d82.png                                         10.02 KB    4.59s
dist/nodejs.77bd994b.png                                         5.87 KB    4.59s
dist/jquery4.6934a131.png                                        4.76 KB    4.59s
dist/js3.7ae0e064.png                                            4.31 KB    4.59s
dist/lotus_favicon_3.1c2d6149.png                                4.19 KB    4.59s
dist/git2.f771b043.png                                           2.33 KB    4.59s
dist/npm.df553ec1.png                                              473 B    4.59s
✨  Done in 11.88s.
```

Follow [React GitHub pages deployment tutorial](https://create-react-app.dev/docs/deployment/#github-pages).

Add to `package.json`:
```json
"homepage": "https://hashbangash.github.io",
"scripts": {
  "start": "parcel serve index.html",
  "build": "parcel build index.html --public-url /",
  "predeploy": "yarn build",
  "deploy": "gh-pages -b master -d dist"
}

```

`yarn add gh-pages`

There are some small glitches I haven't tried to fix yet. I'm using `yarn build` and pushing to master instead of using `yarn deploy`, so I might be able to delete the `yarn predeploy` and `yarn deploy` scripts, but currently unsure. Will fix when I have more sleep. :) I was just very excited that I got it working!
