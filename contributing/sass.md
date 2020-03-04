# Contributing

CodeIgniter uses SASS. Therefore, you will need to install it first.
You can find further instructions on the official website: https://sass-lang.com/install

**The colors used must comply with the graphic charter.**



## Debug toolbar

Open your terminal, and navigate to the repo's root folder. To generate
the CSS file, use the following command:
``sass --no-cache --sourcemap=none source/sass/toolbar.scss dist/css/toolbar.css``

Details:
- ``--no-cache`` is a parameter defined to disable SASS cache, this prevents a "cache" folder from being created
- ``--sourcemap=none`` is a parameter which prevents soucemap files from being generated
- ``source/sass/toolbar.scss`` is the SASS source
- ``dist/css/toolbar.css`` is he CSS destination



## Website

Open your terminal, and navigate to the repo's root folder. To generate
the CSS file, use the following command:
``sass --no-cache --sourcemap=none source/sass/website.scss dist/css/website.css``

Details:
- ``--no-cache`` is a parameter defined to disable SASS cache, this prevents a "cache" folder from being created
- ``--sourcemap=none`` is a parameter which prevents soucemap files from being generated
- ``source/sass/website.scss`` is the SASS source
- ``dist/css/website.css`` is he CSS destination



## "Welcome" page

Open your terminal, and navigate to the repo's root folder. To generate
the CSS file, use the following command:
``sass --no-cache --sourcemap=none source/sass/welcome.scss dist/css/welcome.css``

Details:
- ``--no-cache`` is a parameter defined to disable SASS cache, this prevents a "cache" folder from being created
- ``--sourcemap=none`` is a parameter which prevents soucemap files from being generated
- ``source/sass/welcome.scss`` is the SASS source
- ``dist/css/welcome.css`` is he CSS destination



## Documentation

The documentation is generated using Sphinx and the RTD theme.

**Instructions on how to update the theme**

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
