**Keep in mind that it is a new concept. It is the begining. It will require optimizations.**
**I did 95% of the work on the "framework" side, most of the work remaining is on the "website" side.**

# ci4-design


## Concept

A single SASS source to update:

- The debug toolbar
- The "Welcome" page
- The user guide
- The website

The "codeigniter4/design" repository is a bridge between "codeigniter4/framework" and "codeigniter4/website".

Folders description:
- "contributing": Will contain Markdown documentation
- "dist": Will contain the final files which will be copied to the other repositories
- "source": Will contain all the SCSS, HTML, JPG... files required in the diffrent repositories

This is a proposal. People can suggest a different structure to the group.

All the SASS files have some sort of "namespaced". Meaning, I never used "a{...}", instead I used "#debug-bar a{...}", "header a{...}"... This way, we can decide if we want only one global CSS to be generated.


## Generate the CSS

``sass --no-cache --sourcemap=none source/sass/toolbar.scss dist/css/toolbar.css``

``sass --no-cache --sourcemap=none source/sass/website.scss dist/css/website.css``

``sass --no-cache --sourcemap=none source/sass/welcome.scss dist/css/welcome.css``


## Temporary to-do list

### Already done (but could be improved of course)

On the framework side:
- Converted the debug toolbar to SASS (since v4.0)
- Converted the "Welcome" page to SASS (PR pending)

On the website:
- Graphic charter and design according to the community
- Responsive menu
- Heroe section
- Text content sections
- Footer (but links are missing)
- UI elements: links, buttons and "pre" code

### Still to do

On the framework side:
- Convert the user guide CSS to SASS (already working on this, a first PR is pending, I know exactly what has still to be done)

On the website:
- The site map for the first release: probably max 5-6 pages, maybe static pages first. Advanced features like the tutorials and else will come after, through PRs.
- Menu items accordingly
- The pages' content accordingly, which could include: new types of buttons (eg: "Download now" ? In the menu too ?), some sort of banner (for announcements ?), images... everything that you think is useful to present CI4 in the best way
- The footer's content, the original one (from the "Welcome" page) is displaying debug info, we need something else for the website (probably based on the work done on Trello)
- All automated tasked, from SASS compilation to the copy in the "dist" folder. And then, make copies on the the other repositories
- Etc...
