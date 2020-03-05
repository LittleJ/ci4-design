# ci4-design



## Concept


A single SASS source to update:

- The debug toolbar
- The "Welcome" page
- The user guide
- The website

The "codeigniter4/design" repository is a bridge between "codeigniter4/framework" and "codeigniter4/website".

Folders description:
- "dist": Contains the final files which will be copied to the other repositories
- "source": Contains all the SCSS, HTML, JPG... files required in the diffrent repositories

All styles have some sort of "namespaces". Meaning, we don't use "a{...}", instead we use "#debug-bar a{...}", "header a{...}"... This way, we can include various partials without worrying about conflicts.



## Contribute


CodeIgniter uses SASS. Therefore, you will need to install it first.
You can find further instructions on the official website: https://sass-lang.com/install

Every pull request must:
- Comply to the graphic charter
- Be commented (with the correct style)
- Have the same identation



## Compile SASS files


Open your terminal, and navigate to the repo's root folder. To generate
the CSS file, use the following command:

**For the toolbar**

``sass --no-cache --sourcemap=none source/sass/toolbar.scss dist/css/toolbar.css``

**For the website**

``sass --no-cache --sourcemap=none source/sass/website.scss dist/css/website.css``

**For the "Welcome" page**

``sass --no-cache --sourcemap=none source/sass/welcome.scss dist/css/welcome.css``


Details:
- ``--no-cache`` is a parameter defined to disable SASS cache, this prevents a "cache" folder from being created
- ``--sourcemap=none`` is a parameter which prevents soucemap files from being generated
- ``source/sass/*.scss`` is the SASS source
- ``dist/css/*.css`` is he CSS destination



## Update the RTD theme


**For now, the styles are not integrated to this repository.**

The documentation is generated using Sphinx and the RTD theme.

1/ Backup CI's custom files:
- ``user_guide_src/source/_themes/sphinx_rtd_theme/theme.conf``
- ``user_guide_src/source/_themes/sphinx_rtd_theme/static/css/citheme.css``
- ``user_guide_src/source/_themes/sphinx_rtd_theme/static/js/citheme.js``
- ``user_guide_src/source/_themes/sphinx_rtd_theme/static/img/ci-background.png``
2/ Download the latest version of the RTD theme: https://github.com/readthedocs/sphinx_rtd_theme
3/ Place the latest version in the folder ``user_guide_src/source/_themes/sphinx_rtd_theme/``
3/ Restore CI's custom files

You may want to check if:
- The configuration file ``theme.conf`` has not changed in the latest release of the RTD theme
- The file path to the original CSS (from the RTD theme) is valid in ``citheme.css`` (@import)



## Graphic charter


**Themes**

Dark: `#252525` / `rgb(37, 37, 37)`

Light: `#FFFFFF` / `rgb(255, 255, 255)`


**Glossy colors**

Primary: `#DD4814` / `rgb(221, 72, 20)`

Blue: `#5BC0DE` / `rgb(91, 192, 222)`

Gray: `#434343` / `rgb(67, 67, 67)`

Green: `#9ACE25` / `rgb(154, 206, 37)`

Orange: `#DD8615` / `rgb(221, 134, 21)`


**Matt colors**

Primary: `#EF9090` / `rgb(239, 144, 144)`

Blue: `#D8EAF0` / `rgb(216, 234, 240)`

Gray: `#DFDFDF` / `rgb(223, 223, 223)`

Green: `#DFF0D8` / `rgb(223, 240, 216)`

Orange: `#FDC894` / `rgb(253, 200, 148)`


**Subtle colors**

Primary: `#F9F3F3` / `rgb(249, 243, 243)`

Blue: `#E8EFF1` / `rgb(232, 239, 241)`

Gray: `#FAFAFA` / `rgb(250, 250, 250)`

Green: `#EFF5ED` / `rgb(239, 245, 237)`

Orange: `#F9F2EB` / `rgb(249, 242, 235)`
