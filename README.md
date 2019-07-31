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

# Add test files

cypress\support\po.ts

```ts
// we could place this url into cypress.json as "baseUrl"
const url = 'http://localhost:4200';

export const navigateTo = () => cy.visit(url);

export const getGreeting = () => cy.get('app-root h1');
// export const getGreeting = () => cy.get('[data-test=title]');
```

cypress\integrations\spec.ts

```ts
import { navigateTo, getGreeting } from '../support/po';

describe('Hello Angular', () => {
  beforeEach(navigateTo);

  it('should display welcome message', () => {
    getGreeting().contains('Welcome to');
  });

  it('has 3 links', () => {
    cy.get('app-root li a').should('have.length', 3);
  });
});
```
