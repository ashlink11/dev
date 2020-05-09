# Ash Grevelink's Portfolio
#### Date created: Monday, April 13, 2020
#### Date last modified: Friday, May 8, 2020

# Version 4 Build Process from Dojo Project

I created the [dojo project](https://github.com/hashbangash/dojo) so I could build a toolchain from scratch to develop and build my portfolio

A few instructions were different, since the dojo project builds a React app and this is a Bootstrap web app.

Here are the steps I took in [v4 build process](/v4_build.md).

# Version History

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
#### Version 3 - finished April 23, 2020. Includes:
  - Bill of Tech to README
  - Licensing
  - Vulnerabilities
#### Version 4 -
  - Rebuilt toolchain from scratch with yarn and parcel
  - Also includes Bootstrap, Sass and gh-pages dependencies
  - Resized images so they are never wider than 450px and 530px accordingly
  - All tech is now MIT-Licensed and able to be used commercially
  - All tech is latest version which helps prevent vulnerabilities

***

The repo you are currently viewing is not the repo where all my commit history lives. 130+ commits are [here on this repo](https://github.com/hashbangash/hashbangash.github.io), which in turn has a live link of https://hashbangash.github.io/ (notice there is no `/dev`). I used these multiple repos for experimenting with the different build processes for GitHub user sites (built off `master` branch) and GitHub Pages (built off `gh-pages` branch). I was able to build both using the parcel toolchain, but the configuration is easier with GitHub Pages rather than GitHub user sites at present.

***

# Bill of Technology

[Versions 1, 2, and 3 Bill of Tech](./version_history.md)

### Version 4 (current version):
```
"dependencies": {
  "bootstrap": "^4.4.1",
  "gh-pages": "^2.2.0",
  "jquery": "^3.5.1",
  "popper.js": "^1.16.1"
},
"devDependencies": {
  "parcel": "^2.0.0-alpha.3.2",
  "parcel-bundler": "^1.12.4",
  "sass": "^1.26.5"
},
```

#### Summary
I built the toolchain from scratch with yarn package manager and parcel module bundler from [my dojo project](https://github.com/hashbangash/dojo). Also includes Bootstrap and Sass so I can style my site and gh-pages dependencies so I can deploy it live with GitHub.

###### jQuery
Incredibly valuable JS library that simplifies creating event handlers. Instead of writing complex JS commands to select HTML elements and apply events or styling to them, I can write simple jQuery commands. jQuery has an MIT License.

A little history: In the late '90s, Microsoft Internet Explorer didn't follow ECMA's JavaScript/ECMAScript Standard, so the way developers had to write apps for the web got fragmented. Different browsers implemented features like manipulating the DOM with slightly different language, e.g. `appendChild` vs. `insertChild`. Developers had to write a few different versions of their app for different browsers. That is why John Resig invented the jQuery library in 2006, so that a developer could write the app once and have it work on all browsers. Today, there are still differences between browsers, since the ECMAScript Standard doesn't specify how a browser implements JavaScript, and how complete the implementation is, and when.

From the jQuery license: "You are free to use the Project in any other project (even commercial projects) as long as the copyright header is left intact."

###### Bootstrap
An open-source CSS framework that adds a grid system of containers, rows, and columns so I can easily use traditional CSS features like flexbox within a row, for example. It also has an MIT license.

###### Popper.js
Popper is required dependency for Bootstrap. It has zero dependencies of its own in turn, and helps with positioning of pop-up elements. It has an MIT license.

###### gh-pages
Used for deploying my site live to GitHub's web hosting platform, github.io.

###### parcel, yarn, etc.
[Dojo Project dependencies explained here](https://github.com/hashbangash/dojo/blob/master/wiki/dependencies.md). In short, yarn is a package manager built on top of `npm` and parcel is a "zero-configuration" module bundler. These helped me build a minimalist toolchain from scratch to host this site.

###### Sass
Pre-compiles scss into css, which is why it's a dev dependency rather than a production dependency, because it compiles before the user ever goes to my site. Sass helps writing so I can store variables and nest css styles.

# Vulnerabilities

I created the [dojo project](https://github.com/hashbangash/dojo) in April 2020 so my package manager `yarn` and all my dependencies are updated to the latest versions (written May 6, 2020). This helps prevent vulnerabilites.

My goal for the dojo project was to write a **simple, maintainable toolchain** so I can keep all my dependencies updated when patches come out. GitHub `dependabot` sends out automatic pull requests to bump versions, so hopefully next time this happens, I can successfully merge!

# Software License
My project's software has a [MIT License](https://jquery.org/license/). It is open-source and free (in the sense of 'freedom'). You are free to use this code for commercial use. What's cool about the MIT License is it can be re-licensed under other licenses. The MIT License is compatible with many copyleft licenses, such as the GNU General Public License (GPL), which prevents commercial use.

***

## More about me that's not on my portfolio:

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
