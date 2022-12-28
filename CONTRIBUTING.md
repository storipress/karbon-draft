# Contributing to Karbon
👍🎉 First off, thanks for taking the time to contribute! 🎉👍

**Working on your first Pull Request?** You can learn how from this free series How to Contribute to an Open Source Project on GitHub.

Please join our Slack channel if you have any questions or just want to say hi.

## Project setup
### Prerequisites
For hacking on Karbon you'll need to have Node.js and npm installed.

### Quick and dirty setup
`apm develop Karbon`

This will clone the `Karbon` repository to ~/github unless you set the ATOM_REPOS_HOME environment variable.

### I already cloned it!
If you cloned it somewhere else, you'll want to use apm link --dev within the package directory, followed by apm install to get dependencies.

### Workflow
After pulling upstream changes, make sure to run apm update.

To start hacking, run atom --dev . from the package directory. Cut a branch while you're working then either submit a Pull Request when done or when you want some feedback!

### Running specs
You can run specs by triggering the window:run-package-specs command in Atom. To run tests on the command line use apm test within the package directory.

We use Jasmine for writing specs.

### Typescript
We use Tyepscript for type checking. Before you make a pull request, you should solve any type errors. If you have an error you can't fix after taking a crack at it, feel free to open your PR anyway and ask for help there.

### Build Documentation
To build the website locally run:

npm install gitbook-cli -g
gitbook install
gitbook serve
Open up http://localhost:4000 in your browser to live preview changes in the ./docs/ directory. If you want to add or remove a page in the docs, be sure to edit SUMMARY.md.

For more information take a look at https://toolchain.gitbook.com/setup.html.

### Releasing
npm install
npm run build-commit
apm publish patch
