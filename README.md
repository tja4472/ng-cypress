# NgCypress

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.1.3.

# References

https://www.cypress.io/blog/2017/12/11/an-alternative-to-protractor-for-angular-projects

# Run e2e tests

Terminal 1

```sh
npm run start
```

Terminal 2

```sh
npm run cy:open
```

# Install Cypress

```sh
npm install --save-dev --save-exact cypress@3.4.1
npx cypress open
```

```sh
npm install --save-dev --save-exact @bahmutov/add-typescript-to-cypress@2.1.2
```

package.json

```json
  "scripts": {
    "cy:run": "cypress run",
    "cy:open": "cypress open"
  },
```
