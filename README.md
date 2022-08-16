# vue-template

## Deploying to Github Pages

1. edit vue.config.js:
`module.exports = {
  publicPath: process.env.NODE_ENV === "production" ? "/REPO_NAME/" : "/",
};`

2. Build your project using npm build

3. Run: `git add dist && git commit -m 'adding dist subtree'`
  - This commits our changes to the master branch so that we can create a dist subtree in the next step. Make sure that dist is not included in your .gitignore file!

4. Run: `git subtree push --prefix dist origin gh-pages`
  - This step makes gh-pages a subtree of our master branch. The prefix option specifies the folder that we want for our the subtree. If we take a look at our gh-pages branch, we will see that it is equivalent to being the root of the dist folder.
 


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Reusable Components

- BaseCheckbox
- BaseInput
- BaseRadio
- BaseRadioGroup
- BaseSelect
- DefaultVue
- DefaultService
- Auto-Import-Compnents
- VS Code Lint/Prettier Configurations
