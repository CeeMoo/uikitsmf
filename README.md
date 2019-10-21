# uikitsmf
simplemachinesforum 2.1 getuikit tema entegre less

node_modules/uikit/src/less/smf.less

node_modules/uikit/build/build.js

components Export Folder
`../../scripts/uikit/${file.substring(7, file.length - 3)}`

    const steps = {
        core: () => util.compile('src/js/uikit-core.js', '../../scripts/uikit/uikit-core', {minify}),
        uikit: () => util.compile('src/js/uikit.js', '../../scripts/uikit/uikit', {minify, bundled: true}),
        icons: () => util.icons('{src/images,custom}/icons/*.svg').then(ICONS => util.compile('src/js/icons.js', '../../scripts/uikit/uikit-icons', {
            minify,
            name: 'icons',
            replaces: {ICONS}
        })),
        tests: () => util.compile('tests/js/index.js', 'tests/js/test', {minify, name: 'test'})
    };

node_modules/uikit/build/less.js

    {src: 'src/less/uikit.less', dist: `../../css/uikit/uikit-core${rtl ? '-rtl' : ''}.css`},
    {src: 'src/less/uikit.theme.less', dist: `../../css/uikit/uikit${rtl ? '-rtl' : ''}.css`},
    {src: 'src/less/smf.less', dist: `../../css/index${rtl ? '-rtl' : ''}.css`}


---
## Getting started -- Uikit

You have the following options to get UIkit:

- Download the [latest release](https://github.com/uikit/uikit/releases/latest) with pre-built CSS and JS.
- Install with [npm](https://npmjs.com) to get all source files as they are available on Github: ```npm install uikit```
- Install with [yarn](https://yarnpkg.com/) to get all source files as they are available on Github: ```yarn add uikit```
- Directly load UIkit from [CDNJS](https://cdnjs.com): https://cdnjs.com/libraries/uikit
- Clone the repo to get all source files including build scripts: `git clone git://github.com/uikit/uikit.git`
