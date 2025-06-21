# Contributing

There are many ways to contribute to Able Player, and we welcome and appreciate your help! Here are some options:

## Pull Request Process

- If you spot bugs or have feature requests, please submit them to the [Issues][issues] queue.
- If you have code to contribute, please note that all development occurs on the [develop branch][develop]. This is often many commits ahead of the main branch, so please do all development from *develop*, and submit pull requests there.
- If you are multilingual, please consider translating Able Player into another language! All labels, prompts, messages, and help text for each language are contained within a single file, contained within the */translations* directory.

We particularly appreciate help with any issues in the Issues queue that have been flagged with "help wanted".

## Building the Able Player source

The source JavaScript files for Able Player are in the */scripts* directory, and the source CSS files are in the */styles* directory. These source files are ultimately combined into several different files (in the */build* directory) using [npm][] and [Grunt][]:

```sh
# Install Grunt globally 
npm install -g grunt-cli

# Install project dependencies
npm install

# Build CSS and JS
npm run build
```

The npm and Grunt build process is defined by the *Gruntfile.js* and *package.json* files. (Note that the **version number** is specified in *package.json*, and must be updated when a new version is released).

Files created by the build process are put into the */build* directory:

- **build/ableplayer.js** -
  the default build of *ableplayer.js*
- **build/ableplayer.dist.js** -
  a build of *ableplayer.js* without console logging
- **build/ableplayer.min.js** -
  a minified version of the *dist* file
- **build/ableplayer.min.css** -
  a minified combined version of all Able Player CSS files
- **build/separate-dompurify/ directory** -
   same files as above, except DOMPurify is provided as a separate file rather than bundled to give the option of loading the library separately or using a CDN-hosted version.

## Code of Conduct

All contributors to Able Player are expected to follow our [published Code of Conduct](https://github.com/ableplayer/ableplayer/blob/main/code-of-conduct.md). 