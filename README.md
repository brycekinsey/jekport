# Jekport <!-- omit in toc -->

> "Jekport" is a Jekyll portfolio. More specifically, it's a Jekyll theme for personal websites, portfolios, and resumes.

[![Open Issues](https://badgen.net/github/open-issues/brycekinsey/jekport)](https://github.com/brycekinsey/jekport/issues)
[![License](https://badgen.net/github/license/brycekinsey/jekport)](LICENSE)

[View Demo](https://brycekinsey.github.io/jekport/) · [Request Feature](https://github.com/brycekinsey/jekport/issues)

<!-- TABLE OF CONTENTS -->
## Table of Contents <!-- omit in toc -->

* [About The Project](#about-the-project)
  * [Built With](#built-with)
  * [Features](#features)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
  * [Personalize and Customize](#personalize-and-customize)
    * [_config.yml](#_configyml)
    * [Github Metadata Plugin](#github-metadata-plugin)
    * [_data/*.yml](#_datayml)
    * [Particles.js](#particlesjs)
    * [Favicons](#favicons)
* [Contributing](#contributing)
* [License](#license)
* [Acknowledgements](#acknowledgements)

<!-- ABOUT THE PROJECT -->

## About The Project

<!-- [![Project Screenshot][product-screenshot]](https://brycekinsey.github.io/jekport/)) -->

This is a personal website built with `Jekyll` and optimized for hosting on `Github Pages`. This can be used by professionals, who want to showcase their resume and portfolio. If you want to use this for your own website, fork this repository and then refer to [personalize and customize](#personalize-and-customize).

### Built With

* [Jekyll](https://jekyllrb.com/)

### Features

* Mobile-First Responsive Design
* Animated preloader animation
* Landing Page with animated background with [particles.js](https://vincentgarreau.com/particles.js/), a Typing Carousel and animated social icons
* Dark Neumorphism Design on main content
* [Animations On Scroll](https://michalsnik.github.io/aos/)
* Filterable *Skills* word cloud
* [Github's API](https://developer.github.com/v3/) automatically populating the *Open Source Projects* section
* Gulp dev workflow with [BrowserSync](https://browsersync.io/), [Autoprefixer](https://autoprefixer.github.io/) and `JS` & `SCSS` minifying.
* [Google Analytics](https://analytics.google.com/)

<!-- GETTING STARTED -->

## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

* [NodeJS](https://nodejs.org/en/)
  * If you need to switch between Node versions regurlarly, I would recommend to install Node via [Node Version Manager](https://github.com/nvm-sh/nvm/blob/master/README.md#manual-install).

* [Ruby WITH DevKit ](https://www.ruby-lang.org/)
  * For more information, refer to [this](https://www.ruby-lang.org/en/documentation/installation/#ruby-install).

* [Jekyll](https://jekyllrb.com/)
  * For more information, refer to [this](https://jekyllrb.com/docs/installation/).

```sh
gem install bundler jekyll
```
  
### Installation

> Recommended way: If you want to contribute to this theme or open issues due to problems implementing this on your own, I would recommend forking the repository directly. This makes it easier for me to solve open issues and questions or check pull requests.

1.1: Fork the repository (using the `Fork` button at the top) and then clone the repository

```sh
# Replace {YOUR_USERNAME} with your actual username
git clone https://github.com/{YOUR_USERNAME}/jekport.git
```

or

1.2: Create your own repository (using the green `Use this template` button at the top) and then clone the repository

```sh
# Replace {YOUR_USERNAME}, {YOUR_REPOSITORY} with the actual values
git clone https://github.com/{YOUR_USERNAME}/{YOUR_REPOSITORY}.git
```

2: Change directory into jekport

```sh
cd jekport
```

3: Install dependencies

```sh
yarn
bundle install
```

<!-- USAGE EXAMPLES -->

## Usage

* Run and develop locally with live server at `http://localhost:4000`:
```sh
bundle exec jekyll serve
```
* You can also pass the `--livereload` option to `serve` to automatically refresh the page with each change you make to the source files: 

```sh 
bundle exec jekyll serve --livereload 
```

* Once you're ready to comit and push your changes, first run 
```sh 
bundle exec jekyll build
```
* After committing and pushing your changes, see the `Settings` page of your repository to see where your site is published at via `Github Pages`.

### Personalize and Customize

#### _config.yml

Edit `_config.yml` to personalize your site. For documentation, refer to [docs/config.md](https://github.com/brycekinsey/jekport/blob/main/docs/config.md).

#### Github Metadata Plugin

If you want to automatically have your Github repositories pulled for the *Open Source Projects* section, then you also need to authenticate yourself for the Github Metadata plugin to work.

You need to generate a new personal access token on GitHub:

* Go to the [Github Token site](https://github.com/settings/tokens/new).
* Expand the `Personal access tokens` tab.
  * You can select either the `Fine-grained tokens` or `Tokens (classic)` option.
  * For this guide, I'm going to use the `Fine-grained tokens` option.
* Select `Fine-grained tokens` and then `Generate new token`.
* Enter the token settings. My recommended settings are as follows:
  * `Token name`: JEKYLL_GITHUB_TOKEN
  * `Expiration`: It goes up to a year from today. Select `Custom...` and then set the date for a year from today.
  * `Description`: Token for Jekport's GitHub Metadata plugin.
  * `Resource owner`: Leave it as yourself
  * `Repository access`: Select `All repositories`.
  * `Permissions`: Under Repository Permissions, set `Metadata` to Read-Only access. The remaining permissions can stay on the default `no access`.
* Confirm the token settings and select `Generate token`. Copy the token you see on the page.
* Save your token as an environment variable value and/or as a repository secret. 
  * For local development (off of GitHub), you'll want to save your token as an environment variable value.
    * Create a `.env` file inside your local repository and add your generated variable name (e.g.JEKYLL_GITHUB_TOKEN) and token. It should look like this: `JEKYLL_GITHUB_TOKEN=0YOUR0GENERATED0TOKEN0`
    * Confirm that the `.env` file is included, and uncommented, in the `.gitignore` file.
  * For use on GitHub, you'll want to save your token as a repository secret.
    * Go to your repo's settings, then scroll down to the `Security` section.
    * Expand `Secrets and variables`, select `Actions`, and then select `New repository secret`.
    * Enter the variable name (e.g. `JEKYLL_GITHUB_TOKEN`) in the name field and the token in the secret field. Select `Add secret`.

To complete the configuration for the Github Metadata plugin, you also need to change the value of `repository` inside [_config.yml](https://github.com/brycekinsey/jekport/blob/main/_config.yml). After this, you should the Github Metadata plugin should work properly.

For optimal results, you should make sure that every Github project you want included on this portfolio, has added following information on Github:
* Description
* Homepage link, if there is a live version of it
* Topics

#### _data/*.yml

Edit files inside `_data` to add information to the portfolio. For documentation, refer to [docs/data.md](https://github.com/brycekinsey/jekport/blob/main/docs/data.md).

#### Particles.js

Edit [assets/particles.json](https://github.com/brycekinsey/jekport/blob/main/assets/particles.json) to customize the landing page backgorund animation. For more information, refer to [this](https://github.com/VincentGarreau/particles.js/#options).

#### Favicons

The favicons files are stored in [assets/favicon](https://github.com/brycekinsey/jekport/blob/main/assets/favicon). To update the favicon images:

* Go to the [Real Favicon Generator](https://realfavicongenerator.net/) and `Select your favorite image`.
* Scroll to the bottom and select `Generate your Favicons and HTML code`.
* Under the `HTML5` tab, select option 1: `Download your package: Favicon Package`.
* Unzip the folder and copy every file except `browserconfig.xml`, `mstile-150x150.png` and `safari-pinned-tab.html` to the [assets/favicon](https://github.com/brycekinsey/jekport/blob/mainssets/favicon) folder/directory. 
  * If prompted, select to replace the existing files in the destination.

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project, as described in [Installation](#installation).
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- ACKNOWLEDGEMENTS -->

## Acknowledgements

* Fork of [Long Do's Neumorphism project](https://github.com/longpdo/neumorphism)
* [Font Awesome](https://fontawesome.com/)
* [Normalize.css](https://necolas.github.io/normalize.css/)
* Based Preloader on [Codrin Pavel's](https://codepen.io/zerospree/pen/aCjAz) version
* Typing Carousel by [Gregory Schier](https://codepen.io/gschier/pen/jkivt)
* Social Button Animation by [Stéphane Lyver](https://codepen.io/wouwi/pen/Lwrmi)
* Adapted [Damian Jankowski's](https://codepen.io/dolaron/pen/rNadmOE) color palette for the neumorphism design
* Based Timeline on [Krishna Babu's](https://codepen.io/krishnab/pen/OPwqbW) version
