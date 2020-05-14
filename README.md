#### Date created: Monday, April 13, 2020
#### Date last modified: Friday, May 8, 2020

If you clone this repo, `yarn install` and `yarn start` to get started, then go to <http://localhost:1234/>. For more info on building, check out [the build process](/v4_build.md).

# Version History

#### Version 1 (MVP -- minimum-viable-product) completed April 21, 2020
  - Name, quote, photo.
  - 4 projects
  - Skills section
  - About me section
  - Contact section
  - Mobile-first, responsive, accessible, dark-mode, minimalist design.

#### Version 2 - completed April 22, 2020
  - "About this site" section on accessibility, licensing, and tech.
  - Alt text and title text on all images. All logos have alt text.
  - Story of development for all Projects.
  - In-class presentation link on Data Flow.
  - Ensures all links open in a new tab.
  - Navigation menu to navigate to parts of the page.
  - Focus on accessibility including h1,h2,h3 hierarchy.

#### Version 3 - finished April 23, 2020
  - Bill of Tech to README
  - Licensing
  - Vulnerabilities

#### Version 4 - finished May 8, 2020
  - Rebuilt toolchain from scratch with yarn and parcel
  - Also includes Bootstrap, Sass and gh-pages dependencies
  - Resized images so they are never wider than 450px and 530px accordingly
  - All tech is now MIT-Licensed and able to be used commercially
  - All tech is latest version which helps prevent vulnerabilities

# Dark Theme Design

I used the Pantone 2018 Color of the Year "ultra violet" for my primary color (hex: `#5f4b8b`). Then, I used [Material.io's Color Palette Generator](https://material.io/design/color/the-color-system.html#tools-for-picking-colors) to generate my complementary color (sage green-ish).

![Color Palette](https://user-images.githubusercontent.com/22508682/81463195-93870a00-9185-11ea-8fd8-a2a7f0fe3f0b.png)

I chose a handful of different variants of my primary and complementary colors to [separate surfaces and meet accessibility standards](https://material.io/design/color/dark-theme.html).

I created some [transparent variants with 8-digit hex](https://css-tricks.com/8-digit-hex-codes/) to help express depth on the classic dark gray surface (`#121212`).

![Sass Colors](https://user-images.githubusercontent.com/22508682/81463197-94b83700-9185-11ea-9418-83240ba2a03b.png)

# Bill of Technology

First, I created the [dojo project](https://github.com/hashbangash/dojo). It's a simple web-app built with yarn, Parcel, and React. I created a detailed tutorial so others could build a toolchain from scratch.

Then, using the dojo project tutorial, I rebuilt this portfolio's toolchain. Here are the steps I took in [the build process](/v4_build.md). Here's the [Old Bill of Tech before I rebuilt the app](./version_history.md).

### [yarn](https://yarnpkg.com/) (package manager)
 - "Fast, reliable, and secure dependency management."
 - built by Facebook in 2016

## Dependencies
```
"dependencies": {
  "bootstrap": "^4.4.1",
  "gh-pages": "^2.2.0",
  "jquery": "^3.5.1",
  "popper.js": "^1.16.1"
},
```

### [jQuery](https://jquery.com/)
 - write simple jQuery commands to select HTML elements and modify them instead of complex JavaScript commands
 - jQuery commands work with many different browser DOMs, so you write once and works on all browsers
 - open-source MIT License (in the jQuery source code)
 - John Resig invented the jQuery library in 2006

### [Bootstrap](https://getbootstrap.com/)
 - CSS framework
 - grid system of containers, rows, and columns
 - easily use traditional CSS features like Flexbox within a row, for example
 - open-source MIT License

### [Popper.js](https://popper.js.org/)
 - required dependency for Bootstrap
 - zero dependencies of its own
 - helps with positioning of pop-up elements
 - open-source MIT license

### [gh-pages](https://pages.github.com/)
 - GitHub Pages is a static site hosting service
 - use to deploy my site live to <https://hashbangash.github.io/dev/>

## Development Dependencies
```
"devDependencies": {
  "parcel": "^2.0.0-alpha.3.2",
  "parcel-bundler": "^1.12.4",
  "sass": "^1.26.5"
},
```

### [parcel](https://parceljs.org/)
 - "blazing fast, zero-configuration web application bundler"
 - Ryan Dahl (creator of Node.js and Deno JS frameworks) said that parcel is "really great" in his [10 Things I Regret About Node.js talk](https://www.youtube.com/watch?v=M3BM9TB-8yA) (at 23:20)
 - `parcel` is the CLI tool and `parcel-bundler` is the main library of code

### [Sass](https://sass-lang.com/documentation)
 - "stylesheet language" that pre-compiles scss into css
 - can store variables and nest css styles

# Vulnerabilities

My goal for this project was to write a **simple, maintainble toolchain**.

I used `yarn` for my package manager because it's [more secure than `npm`](https://engineering.fb.com/web/yarn-a-new-package-manager-for-javascript/).

I created the build toolchain (see [dojo project](https://github.com/hashbangash/dojo)) in April 2020 so my package manager `yarn` and all my dependencies are updated to the **latest versions** (written May 8, 2020). This helps prevent vulnerabilites.

GitHub's `dependabot` sends out automatic pull requests to bump versions so I can keep all my dependencies updated when patches come out.

# Software License
My project has a [MIT License](https://jquery.org/license/). It is open-source and free (in the sense of 'freedom'). You are free to use this code for commercial use. What's cool about the MIT License is it can be re-licensed under other licenses. The MIT License is compatible with many copyleft licenses, such as the GNU General Public License (GPL), which prevents commercial use.

## Commit History

The repo you are currently viewing is not the repo where all my commit history lives. 130+ commits are [here on this repo](https://github.com/hashbangash/hashbangash.github.io), which in turn has a live link of <https://hashbangash.github.io/> (notice there is no `/dev`). I used these multiple repos for experimenting with the different build processes for GitHub user sites (built off `master` branch) and GitHub Pages (built off `gh-pages` branch). I was able to build both using the parcel toolchain, but the configuration is easier with GitHub Pages rather than GitHub user sites at present.
