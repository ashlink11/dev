# Ash Grevelink's Portfolio

### April 29, 2020 update:

#### Version 1 (MVP -- minimum-viable-product) completed April 21, 2020. Includes:
  - Name, quote, photo.
  - 4 projects
  - Skills section
  - About me section
  - Contact section
  - Mobile-first, responsive, accessible, dark-mode, minimalist design.

#### Version 2 - completed April 22, 2020. Includes:
  - "About this site" section on accessibility, licensing, and tech.
  - Alt text and title text on all images. All logos have alt text.
  - Story of development for all Projects.
  - In-class presentation link on Data Flow.
  - Ensures all links open in a new tab.
  - Navigation menu to navigate to parts of the page.
  - Focus on accessibility including h1,h2,h3 hierarchy.

#### Version 3 - completed April 24, 2020. Includes:
  - Bill of Tech to README
  - Licensing
  - Vulnerabilities
  - New favicon

#### Version 4: expected completion: May 8, 2020
  - Rebuild the site with React, yarn, and parcel instead of GA's `browser-template`. This build process will be based on the one from my current [dojo project](https://github.com/hashbangash/dojo). This will enable:
    - my portfolio is built on software with a MIT License.
    - more pages with `react-router-dom` so my "about this site" can live on it's own page
    - transform this from a SPA (single-page-app) to a PWA (progressive web-app)
    - address vulnerabilities in the `browser-template` stack and provide a secure site
    - minify (compress) my JS files so they are much smaller
  - Compress all my image files.
  - Add log-in help for all my projects.
  - Add an illustration visualizing my progress over my computing career of skills gained based on [the developer roadmap](https://github.com/kamranahmedse/developer-roadmap).

***

My portfolio site currently lives here with the live link of: https://hashbangash.github.io/dev/.

***

The repo you are currently viewing is not the repo where my commit history lives. My commit history is [here on this repo](https://github.com/hashbangash/hashbangash.github.io), which in turn has a live link of https://hashbangash.github.io/ (notice there is no `/dev`). That version has deployment issues with Bootstrap margins. I hope to address these in a later version of my portfolio. I plan on reading grunt, webpack and Bootstrap documentation and building the dev and production environments from scratch in order to solve these issues. I'm excited for that.

***

# Bill of Technology

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

**babel polyfill**: Transpiles ECMAScript 6+ code to ES5. A polyfill provides modern functionality for older browsers.

The main reason we need polyfills now is because it's common for different browser engines to implement only part of the ECMAScript standard. Modern JavaScript might not be supported by all browsers, so we need to translate the new JavaScript features into older ones.

Babel is a JS compiler that is now broken into separate small packages. I am using just the polyfill package. Babel has an MIT license.

**bootstrap**: An open-source CSS framework that adds a grid system of containers, rows, and columns so I can easily use traditional CSS features like flexbox within a row, for example. It also has an MIT license.

**popper.js**: Popper is required dependency for Bootstrap. It has zero dependencies of its own in turn, and helps with positioning of pop-up elements. It has an MIT license.

### Vulnerabilities
Version 4 will address vulnerabilities, which is a major goal of my [dojo project](https://github.com/hashbangash/dojo).

## [License](LICENSE)

Thir project uses the General Assembly website template called the [browser template](https://git.generalassemb.ly/ga-wdi-boston/browser-template). There are separate licenses for the software and the content.

From the General Assembly [browser template](https://git.generalassemb.ly/ga-wdi-boston/browser-template) license:
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or
alternative licensing, please contact legal@ga.co.

### Software License
My project's software has a [GNU General Public License, version 3](https://www.gnu.org/licenses/gpl-3.0.txt). Specifically, the license is GPL-3.0-or-later.

More info about this GNU GPLv3 license: Copyright © 2007 [Free Software Foundation, Inc.](https://fsf.org/)

All of my other tech dependencies have [MIT license](https://jquery.org/license/). The MIT License is compatible with my project because it can be re-licensed under other licenses. The MIT License is compatible with many copyleft licenses, such as the GNU General Public License (GPL). It is open-source and free (in the sense of 'freedom').

### Content License
The license of General Assembly's content (not software) is [Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/), meaning:

You are free to:
* Share — copy and redistribute the material in any medium or format
* Adapt — remix, transform, and build upon the material

Under the following terms:
* Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
* NonCommercial — You may not use the material for commercial purposes.
* ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

## More about me that's not on my portfolio:

#### General Assembly Software Engineering Bootcamp Topics:
- Project 1 (JavaScript, HTML, CSS, AJAX, jQuery, npm)
- Project 2 (Ruby, Rails, PostgreSQL, HTML, CSS, AJAX, jQuery, npm, Handlebars, Bootstrap)
- Project 3 (JavaScript, Node.js, Express, MongoDB, HTML, CSS, AJAX, jQuery, Handlebars, Bootstrap)
- Project 4 (JavaScript, React (Hooks, JSX, styled-components, Axios), Ruby on Rails, PostgreSQL)
- Personal site (Bootstrap, HTML, CSS, grunt, webpack, npm)

#### Westminster College (Salt Lake City, UT) courses:
- Databases (MySQL)
- Computer Systems (Unix, GNU/Linux, assembly, C)
- Networking (Java)
- Operating Systems (C)
- Software Engineering (Spring, Java, Angular, AGILE)

#### University of Utah courses:
- Intro to Computer Science (hardware, build simple computer)
- Intro to Object-Oriented Programming (Java)
- Data Structures & Algorithms (taken 3 times)
- Deductive Logic
- Calculus I
- Discrete Structures

#### Freelancing Skills:
- Wordpress management
- SEO strategies (image alt tags, metadata, Structured Data, content, keywords, UX design)
- Use of SEO tools
  - Google Search Console
  - Google PageSpeed Insights
  - Google MyBusiness

#### Skills/knowledge from software engineering at Huckabuy (SEO Marketing startup in Park City, UT):
- Remote skills
- LD-JSON Structured Data
- Responsibility for Structured Data on 75+ enterprise customers' websites including SAP App Center, Salesforce AppExchange, Domo, SaltStack, Pluralsight, etc.
- Google search algorithm, crawling & rendering
- SEO strategies & tools (Google Search Console, Ahrefs, Google Lighthouse, Google Analytics, Google PageSpeed Insights)
- Google Cloud Platform architecture (Google App Engine, Kubernetes, etc.)
- Docker
- git & Github
- Teamwork (leader-leader model, "5 Dysfunctions of a Team" book philosophy)

#### Contact info:
- [LinkedIn](https://www.linkedin.com/in/ash-grevelink/)
- [GitHub](https://github.com/hashbangash)
- Greater Boston Area
- ashlink1111@gmail.com
