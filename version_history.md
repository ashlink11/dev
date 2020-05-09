# Versioning History

### Versions 1 to 3 Bill of Technology (April 2020)

### Dependencies
 - [browser template](https://git.generalassemb.ly/ga-wdi-boston/browser-template)
 - jquery
 - bootstrap
 - popper.js
 - babel-polyfill (deprecated)

### Build tools
 - npm
 - grunt
 - webpack

### Vulnerabilities
There were many vulns and I didn't understand the build well enough to bump patches and still keep the dev and prod environments working.

### Licenses

The General Assembly `browser-template` is GNU GPLv3, which means it's open source, but I can't use it for commercial purposes. I wanted to build a portfolio which I could use to find work, so I rebuilt the toolchain in version 4.

### Old README:

I took a Software Engineering Immersive from General Assembly, Boston and I use their front-end [browser template](https://git.generalassemb.ly/ga-wdi-boston/browser-template) as base for this website. The versioning of my dependencies is a bit behind the latest. For example, `babel-polyfill` is deprecated. It was still a great learning opportunity and has given me the knowledge to build my own projects from scratch with versioning maintainability in mind.

I use npm to manage the node modules and packages. [`package.json`](./package.json) has a list of `dependencies` and `devDependencies`. `devDependencies` are tools used for development, not production, and there are 33 of them in this project, including `webpack`, `grunt`, a linter, etc.

```json
"dependencies": {
  "jquery": "^3.3.1",
  "babel-polyfill": "^6.26.0",
  "bootstrap": "^4.1.2",
  "popper.js": "^1.14.3"
}
```

**jQuery**: Incredibly valuable JS library that simplifies creating event handlers. Instead of writing complex JS commands to select HTML elements and apply events or styling to them, I can write simple jQuery commands. jQuery has an MIT License.

A little history: In the late '90s, Microsoft Internet Explorer didn't follow ECMA's JavaScript/ECMAScript Standard, so the way developers had to write apps for the web got fragmented. Different browsers implemented features like manipulating the DOM with slightly different language, e.g. `appendChild` vs. `insertChild`. Developers had to write a few different versions of their app for different browsers. That is why John Resig invented the jQuery library in 2006, so that a developer could write the app once and have it work on all browsers. Today, there are still differences between browsers, since the ECMAScript Standard doesn't specify how a browser implements JavaScript, and how complete the implementation is, and when.

From the jQuery license: "You are free to use the Project in any other project (even commercial projects) as long as the copyright header is left intact."

**babel polyfill**: Transpiles ECMAScript 6+ code to ES5. A polyfill provides modern functionality for older browsers.

The main reason we need polyfills now is because it's common for different browser engines to implement only part of the ECMAScript standard. Modern JavaScript might not be supported by all browsers, so we need to translate the new JavaScript features into older ones.

Babel is a JS compiler that is now broken into separate small packages. I am using just the polyfill package. Babel has an MIT license.

**bootstrap**: An open-source CSS framework that adds a grid system of containers, rows, and columns so I can easily use traditional CSS features like flexbox within a row, for example. It also has an MIT license.

**popper.js**: Popper is required dependency for Bootstrap. It has zero dependencies of its own in turn, and helps with positioning of pop-up elements. It has an MIT license.

## License

Thir project uses the General Assembly website template called the [browser template](https://git.generalassemb.ly/ga-wdi-boston/browser-template). There are separate licenses for the software and the content.

From the General Assembly [browser template](https://git.generalassemb.ly/ga-wdi-boston/browser-template) license:
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or
alternative licensing, please contact legal@ga.co.
