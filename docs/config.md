# Documentation for _config.yml

## General Site Settings

* `title`: This will be displayed as the website's name in your browser tab.
* `description`: This will be meta HTML tag content.
* `url`: The URL of your site.
  * Set this to the protocol & hostname for your site, e.g., 'https://username.github.io'.
* `baseurl`: The subpath of your site
  * Set this to the subpath of your site (if applicable), e.g., '/blog'.
  * Set this to "", if you don't have a baseurl.

*Note: This url field specifies the URL of the site. When combined with baseurl, it helps Jekyll generate the full URLs for assets and links. For example, if url is set to https://username.github.io and baseurl is set to /blog, a relative link to /assets/css/main.css would resolve to https://username.github.io/blog/assets/css/main.css.*

## Landing Page

* `username`: This will displayed on the landing page as your name.

* `typing_text`: This will be text, which will be typed before *scroll down for more*.
  * set this to your job title, e.g. **Fullstack Developer**
* `email`: Your E-Mail address for the email button.
* Social Link buttons:
  * For every social button you want to display, set your username or userid
  * Usernames or ids can usually be taken from your profile links
  * If you do not use one of the following websites, then leave it empty
  * e.g. since I use GitHub and LinkedIn but not Twitter or Codepen, my configs are like this:
    * `github_username`: **brycekinsey**
    * `codepen_username`: 
    * `dev_username`:
    * `linkedin_username`: **bryce-kinsey**
    * `twitter_username`:

## About Me Section

* `show_aboutme_card`:
  * setting this to **true**, will display the About Me section
  * setting this to **false**, will omit the About Me section
* `about_me_title`: The will be displayed as the title in the About Me section
* `about_me_description`: This will be displayed under the title.
  * You can add and style website links with this HTML template inside every **section_description**, e.g. check out the current `about_me_description`:

  ```html
  <a class="highlight-link" href="https://github.com/brycekinsey/jekport" target="_blank" rel="noreferrer"> Github </a>
  ```

## Skills Section

* `show_skills_card`:
  * setting this to **true**, will display the Skills section
  * setting this to **false**, will omit the Skills section
* `about_me_title`: The will be displayed as the title in the Skills section

## Timeline Section

* `show_timeline_card`:
  * setting this to **true**, will display the Timeline section
  * setting this to **false**, will omit the Timeline section
* `timeline_title`: The will be displayed as the title in the Timeline section
* `cv_download_link`: The link where you host your cv.

## Projects Section

* `show_projects_card`:
  * setting this to **true**, will display the Projects section
  * setting this to **false**, will omit the Projects section
* `show_projects`:
  * setting this to **true**, will display your listed projects in _data/projects.yml
  * setting this to **false**, will omit your listed projects
* `projects_title`: The will be displayed as the title of your projects
* `show_os_projects`:
  * setting this to **true**, will display your public projects on github
  * setting this to **false**, will omit your public projects on github
* `os_projects_title`: The will be displayed as the title of your open source (public) projects from GitHub

## Contact Section

* `show_contact_card`:
  * setting this to **true**, will display the Contact section
  * setting this to **false**, will omit the Contact section
* `contact_title`: The will be displayed as the title in the Contact section
* `contact_description`: This will be displayed under the title.

## Github Metadata

* `repository`:
  * Set this to your forked repository
  * e.g. `<user>/<user>.github.io`
* `projects`:
  * `sortby`:
    * set this to **pushed**, if you want to sort your github repositories by time.
    * set this to **stars**, if you want to sort your github repositories by stars.
  * `exclude`:
    * `archived`:
      * setting this to **true**, will exclude archived repositories
      * setting this to **false**, will also display archived repositories
    * `forks`:
      * setting this to **true**, will exclude forked repositories
      * setting this to **false**, will also display forked repositories
    * `projects`: A list of the repository names you want to exclude from the listing.

## Google Analytics

* `id`: Set the id, if you want to track your website with Google Analytics
