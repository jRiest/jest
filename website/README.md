# Run the server

The first time, get all the dependencies loaded via

```
npm install
```

Then, run the server via

```
npm start
Open http://localhost:8080/jest/index.html
```

Anytime you change the contents, just refresh the page and it's going to be updated

# Publish the website

The Jest website is hosted as a GitHub page. A static site is generated by `server/generate.js` and its output is pushed to the `gh-pages` branch by CircleCI whenever `master` is updated.

To deploy the website manually, run the following command as a Git user with write permissions:

```
GIT_USER=jest-bot CIRCLE_PROJECT_USERNAME=facebook CIRCLE_PROJECT_REPONAME=jest npm run gh-pages
```

## Staging

Run the above command against your own fork of `facebook/jest`:

```
GIT_USER=YOUR_GIT_USERNAME CIRCLE_PROJECT_USERNAME=YOUR_GITHUB_USERNAME CIRCLE_PROJECT_REPONAME=jest npm run gh-pages
```
