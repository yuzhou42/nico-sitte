# Personal academic website toturial
Build a personal website using hugo with [hugo-academic](https://github.com/gcushen/hugo-academic) template.

# set up environment
## [install hugo](https://github.com/gohugoio/hugo/releases)
$ snap install hugo --channel=extended
$ add "export PATH=/snap/bin${PATH:+:${PATH}}$" in .bashrc file

## initailize a hugo folder with academic themes
$ hugo new site my_website
$ cd my_website
$ git init
$ git submodule add https://github.com/gcushen/hugo-academic.git themes/academic
$ cp -av themes/academic/exampleSite/* .

# Structure of hugo site 
Here will talk about the folders and files under root folder where we have to do some modification. More detailed info can refer to the comments in each file and the official website [page builder](https://sourcethemes.com/academic/docs/page-builder/#)
1. config/_default
- config.toml: general layout configuration for the page
- language.toml: config languages for the websites
- menus.toml: Set navigation bar on top of the website
  Weight here only get to decide the order in the navigation bar. The order of contents on this page is decided by the widgets files
- params.toml is mainly for the auther info in the first page
   
1. contents
  All the contents will be written here.
- authors
  Each folder under this is the person's infomation with avatar. The website's author can be assigned as one of the person here in the about.md file under home folder
- courses
- home
  Files under home folder work as indexs to organize coutents in subfolders, for example, post, projects, publications etc. There are sevel page types: publication, post, prject, talk ... Note the widget setting as well in order to get the one you want. The plain version of widget refer to the below section.
  - gallery
  A gallery widget
  - about
  Set author information
  - accomplishments
  Certificates for online courses etc
  - contact
  The contact information can be set both here and params.toml
  - demo
  A fancy welcome page demo
  - experience
  Education or working experience
  - featured
  Featured publication, the differnce from the publication is the display type
  - hero
  Fancy page setup demo
  - index
  Settings for home page: type/headless etc.
  - people
  Add people in your group
  - posts
  - projects
  - pulications
  - skills
  - slider
  Easy to use slider on your page.
  - tags
  - talks
- post
- project
- publication
- slides/example
- talk

3. data (empty)
4. layouts (empty)
5. resources
   Generated files
6. static
  Files and images can be put in static folder.
7. themes/academic
   Academeic template from [hugo-academic](https://github.com/gcushen/hugo-academic)
   
## modify your own contents 
### add new contents
- manually
  You can manually create content files (for example as content/<CATEGORY>/<FILE>.<FORMAT>) and provide metadata in them
- by command
  $ cd root-folder-of-your-site
  $ hugo new posts/test.md (for example)
  Then you will get a page looks like this:
``` 
  +++
# A section created with the Blank widget.
widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/ 
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 1  # Order that this section will appear.

# Note: a full width section format can be enabled by commenting out the `title` and `subtitle` with a `#`.
title = "Test"
subtitle = ""

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "1"

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  # color = "navy"
  
  # Background gradient.
  # gradient_start = "DeepSkyBlue"
  # gradient_end = "SkyBlue"
  
  # Background image.
  # image = "image.jpg"  # Name of image in `static/img/`.
  # image_darken = 0.6  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.

  # Text color (true=light or false=dark).
  # text_color_light = true

[design.spacing]
  # Customize the section spacing. Order is top, right, bottom, left.
  # padding = ["0px", "0px", "0px", "0px"]

[advanced]
 # Custom CSS. 
 css_style = ""
 
 # CSS class.
 css_class = ""
+++

[**Add some elements here**](https://sourcethemes.com/academic/docs/writing-markdown-latex/)
```

Noted that the content between "+++" is configuration and below it is the text elements.

## Build static pages
```
$ hugo -D
```
Output will be in ./public/ directory by default

# Usage
## View locally
```
$ hugo server --watch
```
## [Deploy/host on GitHub](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
1. Create a <YOUR-PROJECT> (e.g. blog) repository on GitHub. This repository will contain Hugo’s content and other source files.
2. Create a <USERNAME>.github.io GitHub repository. This is the repository that will contain the fully rendered version of your Hugo website.
3. git clone <YOUR-PROJECT-URL> && cd <YOUR-PROJECT>
4. Paste your existing Hugo project into the new local <YOUR-PROJECT> repository. Make sure your website works locally (hugo server or hugo server -t <YOURTHEME>) and open your browser to http://localhost:1313.
5. Once you are happy with the results:
Press Ctrl+C to kill the server
Before proceeding run rm -rf public to completely remove the public directory
git submodule add -b master https://github.com/<USERNAME>/<USERNAME>.github.io.git public. This creates a git submodule. Now when you run the hugo command to build your site to public, the created public directory will have a different remote origin (i.e. hosted GitHub repository).
7. Make sure the baseURL in your config file is updated with: <USERNAME>.github.io
8. Lateron: run ./deploy.sh "Your optional commit message" to send changes to <USERNAME>.github.io next time.
```
$ ./deploy.sh
```


### functions
Please check out details on the official website, here are only some changes we made often. Remember whenever you wanted to edit something regarding layouts, you will need to create setting file following the structure in the theme submodule under your root layouts. The function set in root will overwrite the one in the submodule.
1. hide widgets on main page: set active = false 
2. order of widgets: set weight parameter, the bigger the lower
3. add web counter
   - copy cooresponding file under themes/academic/layouts/partials, e.g. site_footer.html into the /root/layouts/partials folder.
   - Find a web counter plugin on [freecounterweb](https://www.counter12.com/)
   - copy the html code into file under your root folder.
   - Done!

4. [custom theme](https://sourcethemes.com/academic/docs/customization/#custom-theme)
Choose one frome themes/academic/data/themes/xxx.toml and set theme = "xxx" in config/_default/params.toml. To customize a color theme, copy a theme such as themes/academic/data/themes/minimal.toml to data/themes/my_theme.toml (at the root of your site, not in themes/academic/), creating the data/themes/ folders if they do not already exist.

5. Add TOC for posts/projects etc
   - change this param in the config.toml to set the level of table of content
  ```
    [markup.tableOfContents]
    startLevel = 1
    endLevel = 4
  ```
   - create single.html file under root/layouts/_default and root/layouts/project etc.
   - copy the following content inside the single.html file.
  
  ```
  {{- define "main" -}}
  {{ if .Params.toc }}
  <div class="container-fluid docs">
      <div class="row flex-xl-nowrap">
        <div class="d-none d-xl-block col-xl-2 docs-toc">
          <ul class="nav toc-top">
            <li><a href="#" id="back_to_top" class="docs-toc-title">{{ i18n "on_this_page" }}</a></li>
          </ul>
          {{ .TableOfContents }}
          {{ partial "docs_toc_foot" . }}
        </div>
        <main class="col-12 col-md-0 col-xl-10 py-md-3 pl-md-5 docs-content" role="main">
  {{ end }}
          <article class="article">
              {{ partial "page_header" . }}
              <div class="article-container">
                <div class="article-style">
                  {{ .Content }}
                </div>
                {{ partial "page_footer" . }}
              </div>
          </article>
    {{ if .Params.toc }}
        </main>
      </div>
    </div>
    {{ end }}
  {{- end -}}
  ```

# Links
- [hugo-get-started](https://gohugo.io/getting-started/)