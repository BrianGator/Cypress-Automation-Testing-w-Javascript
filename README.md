# Cypress-Automation-Testing-Framework-Ninja 🥋

A comprehensive Cypress automation testing framework built with JavaScript, designed to master modern web automation testing practices, locator strategies, and advanced Cypress methodologies.

---

## 📋 Table of Contents

### Quick Links
- [📌 Quick Start](#quick-start)
- [🎯 Overview](#overview)
- [✨ Features](#key-features)
- [🛠️ Tech Stack](#tech-stack)

### Setup & Installation
- [📦 Prerequisites](#prerequisites)
- [🚀 Installation](#installation)
- [⚙️ Configuration](#configuration)

### Learning & Development
- [📁 Project Structure](#project-structure)
- [📖 How to Use](#how-to-use)
- [🎓 Cypress Methodologies](#cypress-methodologies-covered)

### Code Examples & Guides
- [💻 Basic Examples](#basic-usage-examples)
- [🏗️ Page Object Model](#page-object-model-pattern)
- [🎯 Advanced Techniques](#advanced-techniques)
- [✅ Assertions & Validations](#assertions--validations-guide)
- [📝 Best Practices Tips](#cypress-best-practices--tips-guide)
- [🔍 Locator Strategies Guide](#locator-strategies-comprehensive-guide)

### Resources & Support
- [📚 Learning Resources](#learning-resources)
- [🤝 Contributing](#contributing)
- [📝 License](#license)

---

## 🎯 Overview

This project is a practice-focused automation testing framework that covers essential Cypress testing concepts and advanced techniques. It demonstrates best practices for writing maintainable, scalable, and reliable end-to-end tests using modern web automation principles.

**Perfect for:**
- Beginners learning Cypress and test automation
- QA professionals transitioning to automation
- Developers wanting to understand E2E testing
- Teams building robust test suites

---

## ✨ Key Features

- **Comprehensive Locator Strategies**: Master CSS selectors, XPath, element attributes, and data attributes
- **Selector Playground**: Interactive testing of selectors before writing test code
- **Advanced Command Chaining**: Learn how to chain Cypress commands effectively
- **Child Element Handling**: Techniques for working with nested and dynamic DOM elements
- **Page Object Model**: Organized test structure using page object pattern
- **Test Automation Best Practices**: Real-world examples and patterns
- **Cross-browser Testing**: Support for Chrome, Firefox, and Edge browsers
- **Custom Commands**: Reusable helper functions for common operations
- **Assertions & Validations**: Comprehensive testing strategies
- **Detailed Examples**: From basic to advanced automation scenarios

---

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|-----------|---------|---------|
| **Cypress** | Latest | End-to-end testing framework |
| **JavaScript (ES6+)** | Modern | Test scripting language |
| **Node.js** | 14+ | Runtime environment |
| **npm** | 6+ | Package manager |
| **Mocha** | Built-in | Test framework (via Cypress) |
| **Chai** | Built-in | Assertion library (via Cypress) |

---

## 📦 Prerequisites

Before getting started, ensure you have the following installed:

- **Node.js** (v14.0.0 or higher) - [Download](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **Git** - Version control system
- **Code Editor** - VS Code recommended
- **Modern Web Browser** - Chrome, Firefox, or Edge

---

## 🚀 Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/BrianGator/Cypress-Automation-Testing-w-Javascript.git
cd Cypress-Automation-Testing-w-Javascript
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Verify Installation
```bash
npx cypress --version
```

### Step 4: Open Cypress (Optional - for verification)
```bash
npm run cypress:open
```

---

## ⚙️ Configuration

### Key Configuration Files

**cypress.config.js** - Main configuration file:
```javascript
module.exports = defineConfig({
  e2e: {
    baseUrl: 'http://localhost:3000',
    viewportWidth: 1280,
    viewportHeight: 720,
    defaultCommandTimeout: 5000,
    requestTimeout: 10000,
    responseTimeout: 10000,
    setupNodeEvents(on, config) {
      // implement node event listeners here
    },
  },
});
```

### Browser Configuration

Run tests on specific browsers:
```bash
# Chrome (default)
npx cypress run --browser chrome

# Firefox
npx cypress run --browser firefox

# Edge
npx cypress run --browser edge

# Electron
npx cypress run --browser electron
```

---

## 📁 Project Structure

```
Cypress-Automation-Testing-w-Javascript/
├── cypress/
│   ├── e2e/                          # End-to-end test files
│   │   ├── smoke-tests/             # Smoke test suite
│   │   ├── functional-tests/        # Functional test suite
│   │   └── regression-tests/        # Regression test suite
│   │
│   ├── support/                      # Support files
│   │   ├── commands.js              # Custom Cypress commands
│   │   ├── e2e.js                   # Global test configuration
│   │   └── helpers/                 # Helper utilities
│   │
│   ├── fixtures/                     # Test data files (JSON, CSV, etc.)
│   │   ├── users.json
│   │   ├── products.json
│   │   └── test-data.json
│   │
│   └── plugins/                      # Cypress plugins configuration
│       └── index.js
│
├── node_modules/                     # Project dependencies
├── cypress.config.js                 # Cypress configuration file
├── package.json                      # Project metadata and dependencies
├── package-lock.json                # Dependency lock file
└── README.md                         # This file
```

---

## 📖 How to Use

### Quick Start

**Interactive Mode** (Recommended for development):
```bash
npm run cypress:open
```

**Headless Mode** (For CI/CD pipelines):
```bash
npm run cypress:run
```

### Running Specific Test Suites

```bash
# Run all tests
npm test

# Run smoke tests only
npm run test:smoke

# Run functional tests only
npm run test:functional

# Run tests in headless mode
npm run test:headless

# Run tests with specific browser
npx cypress run --browser chrome
npx cypress run --browser firefox

# Run specific test file
npx cypress run --spec "cypress/e2e/login.cy.js"

# Run tests matching pattern
npx cypress run --spec "cypress/e2e/**/*login*.cy.js"
```

### Key npm Scripts

Update your `package.json` with these scripts:

```json
"scripts": {
  "cypress:open": "cypress open",
  "cypress:run": "cypress run",
  "test": "cypress run",
  "test:smoke": "cypress run --spec 'cypress/e2e/smoke-tests/**/*.cy.js'",
  "test:functional": "cypress run --spec 'cypress/e2e/functional-tests/**/*.cy.js'",
  "test:regression": "cypress run --spec 'cypress/e2e/regression-tests/**/*.cy.js'",
  "test:headless": "cypress run --headless",
  "test:debug": "cypress run --headed --no-exit"
}
```

---

## 🎓 Cypress Methodologies Covered

### 1. **Locator Strategies** [⬆️ back to top](#table-of-contents)
- CSS Selectors (class, id, attribute, pseudo-selectors)
- XPath expressions
- Data attributes (`data-testid`, `data-qa`)
- Text-based selectors
- Combining selectors
- See: [Locator Strategies Guide](#locator-strategies-comprehensive-guide)

### 2. **Element Interaction** [⬆️ back to top](#table-of-contents)
- `.click()` - Clicking elements
- `.type()` - Typing text input
- `.select()` - Selecting dropdown options
- `.check()` / `.uncheck()` - Checkbox/radio handling
- `.submit()` - Form submission
- `.scroll()` - Scrolling elements into view
- `.hover()` - Hovering over elements

### 3. **Assertions & Validations** [⬆️ back to top](#table-of-contents)
- Element visibility checks
- Text content validation
- Attribute verification
- CSS property assertions
- Network request validation
- See: [Assertions Guide](#assertions--validations-guide)

### 4. **Command Chaining** [⬆️ back to top](#table-of-contents)
- Sequential command execution
- Yielding subjects through chains
- Error handling in chains

### 5. **Handling Child Elements** [⬆️ back to top](#table-of-contents)
- Parent-child relationships
- Navigating DOM hierarchy
- `.children()`, `.parent()`, `.find()` methods
- Dynamic element selection

### 6. **Advanced Techniques** [⬆️ back to top](#table-of-contents)
- Page Object Model pattern
- Custom commands creation
- Fixtures and test data management
- Intercept and stub network requests
- Test hooks (before, beforeEach, after, afterEach)
- See: [Advanced Techniques](#advanced-techniques)

### 7. **Best Practices** [⬆️ back to top](#table-of-contents)
- Test isolation and independence
- Avoiding brittle selectors
- Optimal wait strategies
- Error handling patterns
- Maintainable test code
- See: [Best Practices Guide](#cypress-best-practices--tips-guide)

---

## 💻 Basic Usage Examples

### Example 1: Simple Login Test

```javascript
describe('Login Functionality', () => {
  beforeEach(() => {
    cy.visit('https://example.com/login');
  });

  it('should successfully login with valid credentials', () => {
    // Type username
    cy.get('[data-testid="username-input"]').type('testuser@example.com');
    
    // Type password
    cy.get('[data-testid="password-input"]').type('password123');
    
    // Click login button
    cy.get('button[type="submit"]').click();
    
    // Verify redirect to dashboard
    cy.url().should('include', '/dashboard');
    
    // Verify welcome message
    cy.get('.welcome-message').should('contain', 'Welcome');
  });

  it('should show error message with invalid credentials', () => {
    cy.get('[data-testid="username-input"]').type('invalid@example.com');
    cy.get('[data-testid="password-input"]').type('wrongpassword');
    cy.get('button[type="submit"]').click();
    
    cy.get('.error-message')
      .should('be.visible')
      .and('contain', 'Invalid credentials');
  });
});
```

### Example 2: Form Submission with Validation

```javascript
describe('Contact Form Tests', () => {
  beforeEach(() => {
    cy.visit('https://example.com/contact');
  });

  it('should submit form with valid data', () => {
    // Fill form fields
    cy.get('input[name="firstName"]').type('John');
    cy.get('input[name="lastName"]').type('Doe');
    cy.get('input[name="email"]').type('john@example.com');
    cy.get('textarea[name="message"]').type('This is a test message');
    
    // Select from dropdown
    cy.get('select[name="subject"]').select('General Inquiry');
    
    // Check checkbox
    cy.get('input[name="subscribe"]').check();
    
    // Submit form
    cy.get('button[type="submit"]').click();
    
    // Verify success message
    cy.get('.success-message')
      .should('be.visible')
      .and('contain', 'Thank you for contacting us');
  });

  it('should show validation errors for empty fields', () => {
    cy.get('button[type="submit"]').click();
    
    // Verify all error messages appear
    cy.get('.error').should('have.length', 4);
    cy.get('input[name="firstName"]').should('have.class', 'input-error');
  });
});
```

### Example 3: List Operations & Iterations

```javascript
describe('Product List Tests', () => {
  it('should display all products correctly', () => {
    cy.visit('https://example.com/products');
    
    // Verify number of products
    cy.get('.product-item').should('have.length', 10);
    
    // Iterate through products
    cy.get('.product-item').each((product, index) => {
      cy.wrap(product)
        .find('.product-name')
        .should('not.be.empty');
      
      cy.wrap(product)
        .find('.product-price')
        .should('contain', '$');
    });
  });

  it('should add items to cart', () => {
    cy.visit('https://example.com/products');
    
    // Click add to cart on first 3 products
    cy.get('.product-item').each(($item, index) => {
      if (index < 3) {
        cy.wrap($item).find('button[data-testid="add-to-cart"]').click();
      }
    });
    
    // Verify cart count
    cy.get('[data-testid="cart-count"]').should('contain', '3');
  });
});
```

### Example 4: Dropdown & Multi-select Handling

```javascript
describe('Dropdown Interactions', () => {
  beforeEach(() => {
    cy.visit('https://example.com/settings');
  });

  it('should select option from dropdown', () => {
    // Select by value
    cy.get('select[name="country"]').select('US');
    cy.get('select[name="country"]').should('have.value', 'US');
    
    // Select by text
    cy.get('select[name="state"]').select('California');
    
    // Select by index
    cy.get('select[name="city"]').select(0);
  });

  it('should handle multi-select', () => {
    cy.get('[data-testid="multi-select"]').click();
    
    // Select multiple options
    cy.get('.option').contains('Option 1').click();
    cy.get('.option').contains('Option 2').click();
    cy.get('.option').contains('Option 3').click();
    
    // Verify selections
    cy.get('[data-testid="selected-items"]').should('contain', 'Option 1');
    cy.get('[data-testid="selected-items"]').should('contain', 'Option 2');
  });
});
```

### Example 5: Network Requests & Mocking

```javascript
describe('Network Request Tests', () => {
  it('should intercept and verify API calls', () => {
    // Intercept GET request
    cy.intercept('GET', '/api/users', {
      statusCode: 200,
      body: [
        { id: 1, name: 'User 1' },
        { id: 2, name: 'User 2' }
      ]
    }).as('getUsers');

    cy.visit('https://example.com/users');
    
    // Wait for the request
    cy.wait('@getUsers');
    
    // Verify data is displayed
    cy.get('.user-item').should('have.length', 2);
  });

  it('should handle network errors', () => {
    // Intercept with error response
    cy.intercept('POST', '/api/login', {
      statusCode: 401,
      body: { error: 'Unauthorized' }
    }).as('loginFail');

    cy.visit('https://example.com/login');
    cy.get('button[type="submit"]').click();
    
    cy.wait('@loginFail');
    cy.get('.error-message').should('contain', 'Unauthorized');
  });

  it('should verify request payload', () => {
    cy.intercept('POST', '/api/users', (req) => {
      // Verify request body
      expect(req.body).to.include({
        email: 'test@example.com'
      });
      
      req.reply({
        statusCode: 201,
        body: { id: 123, ...req.body }
      });
    }).as('createUser');

    cy.visit('https://example.com/create-user');
    cy.get('input[name="email"]').type('test@example.com');
    cy.get('button[type="submit"]').click();
    
    cy.wait('@createUser');
  });
});
```

[⬆️ back to top](#table-of-contents)

---

## 🏗️ Page Object Model Pattern

The Page Object Model is a design pattern that improves test maintenance and reduces code duplication.

### Basic Page Object Example

```javascript
// pages/LoginPage.js
export class LoginPage {
  // Selectors
  usernameInput = '[data-testid="username-input"]';
  passwordInput = '[data-testid="password-input"]';
  loginButton = 'button[type="submit"]';
  errorMessage = '.error-message';
  welcomeMessage = '.welcome-message';

  // Navigation
  navigate() {
    cy.visit('https://example.com/login');
    return this;
  }

  // Actions
  enterUsername(username) {
    cy.get(this.usernameInput).type(username);
    return this;
  }

  enterPassword(password) {
    cy.get(this.passwordInput).type(password);
    return this;
  }

  clickLoginButton() {
    cy.get(this.loginButton).click();
    return this;
  }

  // Assertions / Verifications
  verifyLoginSuccess() {
    cy.url().should('include', '/dashboard');
    cy.get(this.welcomeMessage).should('be.visible');
    return this;
  }

  verifyLoginError(errorText) {
    cy.get(this.errorMessage)
      .should('be.visible')
      .and('contain', errorText);
    return this;
  }

  verifyUrlChange(expectedUrl) {
    cy.url().should('include', expectedUrl);
    return this;
  }
}

// Test usage
import { LoginPage } from '../pages/LoginPage';

describe('Login Tests with Page Object Model', () => {
  const loginPage = new LoginPage();

  it('should login successfully', () => {
    loginPage
      .navigate()
      .enterUsername('testuser@example.com')
      .enterPassword('password123')
      .clickLoginButton()
      .verifyLoginSuccess();
  });

  it('should show error with invalid credentials', () => {
    loginPage
      .navigate()
      .enterUsername('invalid@example.com')
      .enterPassword('wrongpassword')
      .clickLoginButton()
      .verifyLoginError('Invalid credentials');
  });
});
```

### Advanced Page Object with Reusable Methods

```javascript
// pages/BasePage.js
export class BasePage {
  /**
   * Generic method to fill text input
   */
  fillInput(selector, text) {
    cy.get(selector).clear().type(text);
    return this;
  }

  /**
   * Generic method to select dropdown
   */
  selectFromDropdown(selector, value) {
    cy.get(selector).select(value);
    return this;
  }

  /**
   * Generic method to click element
   */
  clickElement(selector) {
    cy.get(selector).click();
    return this;
  }

  /**
   * Generic method to verify text
   */
  verifyText(selector, expectedText) {
    cy.get(selector).should('contain', expectedText);
    return this;
  }

  /**
   * Generic method to verify element visibility
   */
  verifyElementVisible(selector) {
    cy.get(selector).should('be.visible');
    return this;
  }

  /**
   * Wait for element to be visible
   */
  waitForElement(selector, timeout = 5000) {
    cy.get(selector, { timeout }).should('be.visible');
    return this;
  }
}

// pages/ProductPage.js
import { BasePage } from './BasePage';

export class ProductPage extends BasePage {
  productItem = '.product-item';
  productName = '.product-name';
  productPrice = '.product-price';
  addToCartBtn = '[data-testid="add-to-cart"]';
  cartCount = '[data-testid="cart-count"]';

  navigateToProducts() {
    cy.visit('https://example.com/products');
    return this;
  }

  verifyProductCount(count) {
    cy.get(this.productItem).should('have.length', count);
    return this;
  }

  addProductToCart(productIndex) {
    cy.get(this.productItem)
      .eq(productIndex)
      .find(this.addToCartBtn)
      .click();
    return this;
  }

  verifyCartItemCount(count) {
    cy.get(this.cartCount).should('contain', count.toString());
    return this;
  }
}

// Test with extended Page Object
import { ProductPage } from '../pages/ProductPage';

describe('Product Tests', () => {
  const productPage = new ProductPage();

  it('should display products and add to cart', () => {
    productPage
      .navigateToProducts()
      .verifyProductCount(10)
      .addProductToCart(0)
      .addProductToCart(1)
      .verifyCartItemCount(2);
  });
});
```

[⬆️ back to top](#table-of-contents)

---

## 🎯 Advanced Techniques

### Custom Commands

Create reusable custom commands in `cypress/support/commands.js`:

```javascript
// cypress/support/commands.js

/**
 * Login custom command
 * Usage: cy.login('email@example.com', 'password')
 */
Cypress.Commands.add('login', (email, password) => {
  cy.visit('https://example.com/login');
  cy.get('[data-testid="username-input"]').type(email);
  cy.get('[data-testid="password-input"]').type(password);
  cy.get('button[type="submit"]').click();
  cy.url().should('include', '/dashboard');
});

/**
 * Logout custom command
 * Usage: cy.logout()
 */
Cypress.Commands.add('logout', () => {
  cy.get('[data-testid="logout-btn"]').click();
  cy.url().should('include', '/login');
});

/**
 * Fill form custom command
 * Usage: cy.fillForm({ email: 'test@example.com', password: 'pass123' })
 */
Cypress.Commands.add('fillForm', (formData) => {
  Object.keys(formData).forEach((key) => {
    cy.get(`[name="${key}"]`).type(formData[key]);
  });
});

/**
 * Upload file custom command
 * Usage: cy.uploadFile('input[name="file"]', 'path/to/file.pdf')
 */
Cypress.Commands.add('uploadFile', (selector, filePath) => {
  cy.get(selector).selectFile(filePath);
});

/**
 * Table row interaction
 * Usage: cy.getTableRow({ name: 'John Doe' }).find('button').click()
 */
Cypress.Commands.add('getTableRow', (rowData) => {
  let selector = 'table tbody tr';
  
  Object.keys(rowData).forEach((key) => {
    selector += `:contains("${rowData[key]}")`;
  });
  
  return cy.get(selector);
});

/**
 * Check if element has class
 * Usage: cy.get('button').should(haveClass('active'))
 */
Cypress.Commands.add('haveClass', { prevSubject: true }, (subject, className) => {
  return subject.hasClass(className);
});
```

Using Custom Commands:

```javascript
describe('Using Custom Commands', () => {
  it('should use custom login command', () => {
    cy.login('user@example.com', 'password123');
    cy.get('.welcome-message').should('be.visible');
  });

  it('should fill and submit form', () => {
    cy.visit('https://example.com/register');
    cy.fillForm({
      email: 'new@example.com',
      password: 'password123',
      confirmPassword: 'password123'
    });
    cy.get('button[type="submit"]').click();
  });

  it('should upload file', () => {
    cy.visit('https://example.com/upload');
    cy.uploadFile('input[type="file"]', 'cypress/fixtures/document.pdf');
    cy.get('.success-message').should('be.visible');
  });

  it('should interact with table rows', () => {
    cy.visit('https://example.com/users');
    cy.getTableRow({ name: 'John Doe' })
      .find('button[data-action="edit"]')
      .click();
  });
});
```

### Conditional Testing & Retries

```javascript
describe('Conditional Testing', () => {
  it('should handle conditional scenarios', () => {
    cy.visit('https://example.com/checkout');
    
    // Check if coupon input exists and fill it
    cy.get('body').then((body) => {
      if (body.find('input[name="coupon"]').length > 0) {
        cy.get('input[name="coupon"]').type('SAVE10');
        cy.get('button[data-action="apply-coupon"]').click();
      }
    });
    
    cy.get('button[type="submit"]').click();
  });

  it('should retry failed assertion', () => {
    cy.visit('https://example.com/data');
    
    // Retry assertion up to 3 times
    cy.get('.data-item', { timeout: 10000 })
      .should('have.length.greaterThan', 0);
  });
});
```

### API Testing & Fixtures

```javascript
// cypress/fixtures/users.json
{
  "users": [
    { "id": 1, "name": "John Doe", "email": "john@example.com" },
    { "id": 2, "name": "Jane Smith", "email": "jane@example.com" }
  ]
}

// Test using fixtures
describe('API & Fixture Tests', () => {
  it('should load data from fixture', () => {
    cy.fixture('users').then((userData) => {
      cy.intercept('GET', '/api/users', userData).as('getUsers');
      
      cy.visit('https://example.com/users');
      cy.wait('@getUsers');
      
      cy.get('.user-item').should('have.length', 2);
    });
  });

  it('should work with multiple fixtures', () => {
    cy.fixture('users').as('userData');
    cy.fixture('products').as('productData');
    
    cy.get('@userData').then((users) => {
      cy.log('Users:', users);
    });
  });
});
```

[⬆️ back to top](#table-of-contents)

---

## ✅ Assertions & Validations Guide

Cypress provides powerful assertion capabilities through Chai assertions.

### Common Assertions

```javascript
describe('Comprehensive Assertion Examples', () => {
  beforeEach(() => {
    cy.visit('https://example.com/test-page');
  });

  describe('Element Visibility & Existence', () => {
    it('should verify element visibility', () => {
      cy.get('.visible-element').should('be.visible');
      cy.get('.hidden-element').should('not.be.visible');
      cy.get('.element').should('exist');
      cy.get('.missing-element').should('not.exist');
    });

    it('should verify element states', () => {
      cy.get('input[name="email"]').should('be.enabled');
      cy.get('input[name="disabled"]').should('be.disabled');
      cy.get('input[type="checkbox"]').should('be.checked');
      cy.get('input[type="radio"]').should('not.be.checked');
    });

    it('should verify multiple elements', () => {
      cy.get('.item').should('have.length', 5);
      cy.get('.item').should('have.length.greaterThan', 3);
      cy.get('.item').should('have.length.lessThan', 10);
    });
  });

  describe('Text Content Assertions', () => {
    it('should verify text content', () => {
      cy.get('h1').should('have.text', 'Welcome');
      cy.get('p').should('contain', 'important information');
      cy.get('label').should('contain.text', 'Email');
    });

    it('should verify text case', () => {
      cy.get('.title').should('contain', 'Welcome');
      cy.get('.title').invoke('text').should('include', 'Welcome');
    });
  });

  describe('Attribute Assertions', () => {
    it('should verify element attributes', () => {
      cy.get('input[name="email"]').should('have.attr', 'type', 'email');
      cy.get('a[href]').should('have.attr', 'href');
      cy.get('button').should('have.attr', 'data-testid');
    });

    it('should verify attribute values', () => {
      cy.get('[role="button"]').should('have.attr', 'role', 'button');
      cy.get('[aria-label]').should('have.attr', 'aria-label');
    });

    it('should verify dynamic attributes', () => {
      cy.get('input').should('have.attr', 'placeholder', 'Enter email');
      cy.get('button').should('have.attr', 'disabled');
      cy.get('button').should('not.have.attr', 'disabled');
    });
  });

  describe('CSS & Style Assertions', () => {
    it('should verify CSS classes', () => {
      cy.get('button').should('have.class', 'btn-primary');
      cy.get('button').should('not.have.class', 'disabled');
    });

    it('should verify CSS properties', () => {
      cy.get('.hidden').should('have.css', 'display', 'none');
      cy.get('.text-red').should('have.css', 'color', 'rgb(255, 0, 0)');
      cy.get('.container').should('have.css', 'padding', '16px');
    });

    it('should verify element size & position', () => {
      cy.get('.box').should('have.css', 'width', '200px');
      cy.get('.box').should('have.css', 'height', '100px');
      cy.get('.box').invoke('width').should('be.greaterThan', 100);
    });
  });

  describe('Form Element Assertions', () => {
    it('should verify input values', () => {
      cy.get('input[name="email"]').type('test@example.com');
      cy.get('input[name="email"]').should('have.value', 'test@example.com');
    });

    it('should verify select values', () => {
      cy.get('select[name="country"]').select('US');
      cy.get('select[name="country"]').should('have.value', 'US');
    });

    it('should verify textarea content', () => {
      cy.get('textarea[name="message"]').type('Test message');
      cy.get('textarea[name="message"]').should('have.value', 'Test message');
    });

    it('should verify checkbox/radio states', () => {
      cy.get('input[type="checkbox"]').check();
      cy.get('input[type="checkbox"]').should('be.checked');
      
      cy.get('input[type="radio"]').check('option1');
      cy.get('input[type="radio"]').should('have.value', 'option1');
    });
  });

  describe('List & Collection Assertions', () => {
    it('should verify list items', () => {
      cy.get('ul li').should('have.length', 5);
      cy.get('ul li').first().should('contain', 'First Item');
      cy.get('ul li').last().should('contain', 'Last Item');
    });

    it('should verify each list item', () => {
      cy.get('table tbody tr').each((row) => {
        cy.wrap(row).find('td').should('have.length', 4);
        cy.wrap(row).find('td').first().should('not.be.empty');
      });
    });

    it('should verify all items match criteria', () => {
      cy.get('.product-price').each(($el) => {
        cy.wrap($el).invoke('text').then((text) => {
          expect(text).to.match(/^\$\d+\.\d{2}$/);
        });
      });
    });
  });

  describe('URL & Navigation Assertions', () => {
    it('should verify URL changes', () => {
      cy.visit('https://example.com/home');
      cy.get('a[href="/about"]').click();
      cy.url().should('include', '/about');
    });

    it('should verify URL patterns', () => {
      cy.url().should('match', /example\.com\/users\/\d+/);
      cy.url().should('eq', 'https://example.com/dashboard');
    });
  });

  describe('Complex Assertions', () => {
    it('should use custom assertions', () => {
      cy.get('button').then(($btn) => {
        expect($btn).to.have.class('btn-primary');
        expect($btn).to.contain('Click Me');
        expect($btn).to.be.enabled;
      });
    });

    it('should chain multiple assertions', () => {
      cy.get('.user-card')
        .should('be.visible')
        .and('contain', 'John Doe')
        .and('have.class', 'active');
    });

    it('should use logical assertions', () => {
      cy.get('.status').then(($el) => {
        const status = $el.text();
        expect(status).to.be.oneOf(['active', 'pending', 'inactive']);
      });
    });
  });
});
```

[⬆️ back to top](#table-of-contents)

---

## 🔍 Locator Strategies Comprehensive Guide

### 1. CSS Selectors (Recommended)

```javascript
describe('CSS Selector Examples', () => {
  it('should use various CSS selectors', () => {
    // By class
    cy.get('.button-primary').click();
    
    // By ID
    cy.get('#submit-btn').click();
    
    // By attribute
    cy.get('[type="email"]').type('test@example.com');
    cy.get('[data-testid="login-btn"]').click();
    
    // By attribute value matching
    cy.get('[class*="btn"]'); // Contains
    cy.get('[class^="btn"]'); // Starts with
    cy.get('[class$="primary"]'); // Ends with
    
    // Pseudo-selectors
    cy.get('li:first-child').should('contain', 'First');
    cy.get('li:last-child').should('contain', 'Last');
    cy.get('button:nth-child(3)').click();
    cy.get('input:not([type="hidden"])');
    
    // Combining selectors
    cy.get('form input[type="email"]').type('test@example.com');
    cy.get('button.primary:not(.disabled)').click();
    cy.get('div.container > button.primary').click(); // Direct child
    cy.get('div.container button.primary').click(); // Any descendant
  });
});
```

### 2. Data Attributes (Best Practice)

```javascript
describe('Data Attribute Selectors (BEST PRACTICE)', () => {
  it('should use data-testid for reliable selectors', () => {
    // Recommended for test automation
    cy.get('[data-testid="email-input"]').type('test@example.com');
    cy.get('[data-testid="password-input"]').type('password123');
    cy.get('[data-testid="submit-button"]').click();
    
    // Alternative data attributes
    cy.get('[data-qa="user-profile"]').should('be.visible');
    cy.get('[data-test="notification"]').should('contain', 'Success');
  });
});
```

### 3. XPath (When CSS isn't sufficient)

```javascript
describe('XPath Selectors', () => {
  it('should use XPath when necessary', () => {
    // Absolute XPath (fragile - avoid)
    cy.xpath('/html/body/div/button').click();
    
    // Relative XPath (better)
    cy.xpath('//button[@id="submit"]').click();
    
    // By text content
    cy.xpath('//button[contains(text(), "Submit")]').click();
    cy.xpath('//a[text()="Login"]').click();
    
    // By attribute
    cy.xpath('//input[@type="email"]').type('test@example.com');
    
    // By parent relationship
    cy.xpath('//form//button[@type="submit"]').click();
    cy.xpath('//button[../@id="form-container"]').click();
    
    // By sibling relationship
    cy.xpath('//label[text()="Email"]/following-sibling::input').type('test@example.com');
    
    // By position
    cy.xpath('(//button[@class="primary"])[1]').click(); // First button
    cy.xpath('(//button[@class="primary"])[last()]').click(); // Last button
    
    // Complex XPath
    cy.xpath('//div[@class="user-item" and contains(@data-id, "123")]//button').click();
  });
});
```

### 4. Cy.contains() - Text-Based Selection

```javascript
describe('Text-based Selection with contains()', () => {
  it('should select elements by text content', () => {
    // By exact text
    cy.contains('Login').click();
    cy.contains('button', 'Submit').click();
    
    // By partial text
    cy.contains('Welcome to').should('be.visible');
    
    // Case-insensitive
    cy.contains('login', { matchCase: false }).click();
    
    // Regex
    cy.contains(/Sign (In|Up)/).click();
    
    // With selector specificity
    cy.contains('button.primary', 'Click Me').click();
  });
});
```

### 5. Selector Best Practices & Anti-Patterns

```javascript
describe('Selector Best Practices', () => {
  it('GOOD: Use stable, test-friendly selectors', () => {
    // ✅ Good - Uses data-testid (explicit for testing)
    cy.get('[data-testid="user-email"]').type('test@example.com');
    
    // ✅ Good - Uses semantic HTML
    cy.get('button[aria-label="Close dialog"]').click();
    
    // ✅ Good - Uses class names unlikely to change
    cy.get('.form-submit-button').click();
  });

  it('BAD: Avoid brittle selectors', () => {
    // ❌ Bad - Brittle DOM hierarchy selectors
    // cy.get('div > div > div > button').click();
    
    // ❌ Bad - Inline styles (change frequently)
    // cy.get('[style="color: red;"]');
    
    // ❌ Bad - Index-based selectors (order can change)
    // cy.get('button').eq(2).click(); // Unless necessary
    
    // ❌ Bad - Position-dependent (fragile)
    // cy.get('button:nth-child(5)').click();
    
    // ❌ Bad - Dynamic content selectors
    // cy.get(`button.${dynamicClassName}`);
  });

  it('should handle dynamic and generated content', () => {
    // For generated elements, use partial matching
    cy.get('[id^="user-"]').should('be.visible');
    cy.get('[class*="active"]').click();
    
    // Use within context
    cy.get('.form').within(() => {
      cy.get('input[type="email"]').type('test@example.com');
      cy.get('button[type="submit"]').click();
    });
    
    // Use cy.contains for dynamic text
    cy.contains('Saved successfully').should('be.visible');
  });
});
```

### 6. Advanced Locator Combinations

```javascript
describe('Advanced Locator Patterns', () => {
  it('should chain selectors for precision', () => {
    // Filter by state
    cy.get('button').filter('.primary').click();
    
    // Find within context
    cy.get('.user-card').find('[data-testid="edit-btn"]').click();
    
    // Get parent elements
    cy.get('input[invalid]').parents('form').submit();
    
    // Get siblings
    cy.get('label').contains('Email').siblings('input').type('test@example.com');
    
    // Get closest ancestor
    cy.get('.error-message').closest('.form-group').should('have.class', 'error');
  });

  it('should use within for scoped selection', () => {
    cy.get('.modal').within(() => {
      cy.get('input[type="email"]').type('test@example.com');
      cy.get('input[type="password"]').type('password123');
      cy.get('button[type="submit"]').click();
    });
  });

  it('should combine multiple selection strategies', () => {
    // Start with parent, then find children
    cy.get('[data-testid="user-list"]')
      .find('[data-testid="user-item"]')
      .first()
      .click();
    
    // Filter results
    cy.get('button')
      .filter(':not([disabled])')
      .first()
      .click();
  });
});
```

### Selector Recommendation Matrix

| Scenario | Recommended Selector | Example |
|----------|---------------------|---------|
| Test-specific elements | data-testid | `[data-testid="submit-btn"]` |
| Semantic elements | HTML5 selectors | `button[type="submit"]` |
| By label text | cy.contains + label | `cy.contains('Email')` |
| Form inputs | name or data-testid | `input[name="email"]` |
| Links | href or text | `a[href="/about"]` |
| Avoid | Index or DOM depth | ~~`div > div > button`~~ |
| Fallback | XPath or parent scope | `//button[@id="x"]` |

[⬆️ back to top](#table-of-contents)

---

## 📝 Cypress Best Practices & Tips Guide

### 1. **Test Isolation & Independence** ⭐

```javascript
// ✅ GOOD: Each test is independent
describe('User Management', () => {
  beforeEach(() => {
    // Clear data before each test
    cy.clearCookies();
    cy.clearLocalStorage();
    
    // Start fresh for each test
    cy.visit('https://example.com');
  });

  it('should create user', () => {
    cy.createUser({ name: 'John', email: 'john@test.com' });
    cy.get('.success-message').should('be.visible');
  });

  it('should delete user (independent from create)', () => {
    cy.createUser({ name: 'Jane', email: 'jane@test.com' });
    cy.get('button[data-action="delete"]').click();
    cy.get('.confirmation-dialog').should('be.visible');
  });
});

// ❌ BAD: Tests depend on each other
describe('User Management (Anti-pattern)', () => {
  it('should create user', () => {
    cy.visit('https://example.com');
    cy.createUser({ name: 'John', email: 'john@test.com' });
  });

  it('should edit the user from previous test', () => {
    // This test FAILS if previous test fails
    cy.get('.user-row').first().find('button[data-action="edit"]').click();
  });
});
```

### 2. **Smart Waiting Strategies** ⭐

```javascript
describe('Waiting Best Practices', () => {
  it('GOOD: Wait for element with condition', () => {
    // ✅ Wait for element to exist and be visible
    cy.get('.modal', { timeout: 10000 }).should('be.visible');
    
    // ✅ Wait for API response
    cy.intercept('POST', '/api/users').as('createUser');
    cy.get('button[type="submit"]').click();
    cy.wait('@createUser');
    
    // ✅ Wait for URL change
    cy.url().should('include', '/dashboard');
    
    // ✅ Wait for specific state
    cy.get('[data-testid="loading"]').should('not.exist');
  });

  it('BAD: Hard-coded waits (anti-pattern)', () => {
    // ❌ Avoid hard waits
    // cy.wait(3000); // Brittle and slow
    
    // ❌ Avoid waiting for invisible elements
    // cy.get('.modal', { timeout: 0 });
  });

  it('should handle loading states correctly', () => {
    cy.intercept('GET', '/api/data', (req) => {
      // Simulate network delay
      req.reply((res) => {
        res.delay(1000);
        res.send({ data: [] });
      });
    }).as('loadData');

    cy.visit('https://example.com/data');
    
    // Wait for loading to complete
    cy.get('[data-testid="loading-spinner"]').should('not.exist');
    cy.get('[data-testid="data-table"]').should('be.visible');
    
    cy.wait('@loadData');
  });
});
```

### 3. **Avoiding Flaky Tests** ⭐

```javascript
describe('Flaky Test Prevention', () => {
  it('GOOD: Reliable test with explicit waits', () => {
    cy.visit('https://example.com/checkout');
    
    // Wait for element to be clickable
    cy.get('button[data-action="proceed"]')
      .should('not.be.disabled')
      .click();
    
    // Wait for navigation
    cy.url().should('include', '/payment');
    
    // Wait for content to load
    cy.get('[data-testid="payment-form"]')
      .should('be.visible')
      .within(() => {
        cy.get('input[name="card"]').type('4111111111111111');
      });
  });

  it('BAD: Flaky test with insufficient waits', () => {
    // ❌ Element might not be ready
    // cy.get('button').click(); // Too fast
    
    // ❌ Assuming element exists without waiting
    // cy.get('.element').type('text'); // Might not exist yet
    
    // ❌ Not waiting for dynamic content
    // cy.get('.data-table tr').should('have.length', 10); // Race condition
  });

  it('should handle asynchronous operations', () => {
    // Intercept API calls
    cy.intercept('POST', '/api/process', {
      statusCode: 200,
      delay: 2000,
      body: { status: 'processing' }
    }).as('processRequest');

    cy.visit('https://example.com/process');
    cy.get('button[data-action="process"]').click();
    
    // Wait for the specific API call
    cy.wait('@processRequest');
    
    // Verify response handling
    cy.get('[data-testid="status-message"]')
      .should('contain', 'Processing')
      .and('be.visible');
  });
});
```

### 4. **Error Handling & Recovery** ⭐

```javascript
describe('Error Handling Best Practices', () => {
  it('should handle network errors gracefully', () => {
    cy.intercept('GET', '/api/users', { statusCode: 500 }).as('getUsers');
    
    cy.visit('https://example.com/users');
    cy.wait('@getUsers');
    
    cy.get('.error-message')
      .should('be.visible')
      .and('contain', 'Error loading users');
    
    cy.get('button[data-action="retry"]').click();
    
    // Override the intercept for retry
    cy.intercept('GET', '/api/users', {
      statusCode: 200,
      body: { users: [] }
    });
    
    cy.wait('@getUsers');
  });

  it('should validate before interaction', () => {
    cy.visit('https://example.com/form');
    
    // Verify form exists before filling
    cy.get('form[data-testid="contact-form"]')
      .should('exist')
      .within(() => {
        cy.get('input[name="email"]').should('be.enabled');
        cy.get('textarea[name="message"]').should('be.enabled');
      });
  });

  it('should handle optional elements', () => {
    cy.get('body').then(($body) => {
      // Element might not always exist
      if ($body.find('.optional-banner').length > 0) {
        cy.get('.optional-banner button[aria-label="close"]').click();
      }
    });
    
    // Continue with test
    cy.get('[data-testid="main-content"]').should('be.visible');
  });
});
```

### 5. **Performance Optimization** ⭐

```javascript
describe('Performance Best Practices', () => {
  it('should batch assertions', () => {
    cy.visit('https://example.com/dashboard');
    
    // ✅ Good: Batch related operations
    cy.get('[data-testid="user-card"]').then(($card) => {
      cy.wrap($card)
        .find('.user-name')
        .should('contain', 'John Doe');
      
      cy.wrap($card)
        .find('.user-email')
        .should('contain', 'john@example.com');
      
      cy.wrap($card)
        .find('.user-status')
        .should('have.class', 'active');
    });
  });

  it('should avoid unnecessary page visits', () => {
    // ✅ Visit once, perform multiple tests
    cy.visit('https://example.com/profile');
    
    cy.get('[data-testid="edit-btn"]').click();
    cy.get('input[name="name"]').clear().type('New Name');
    cy.get('button[type="submit"]').click();
    cy.get('.success-message').should('be.visible');
    
    // ✅ Use localStorage/sessionStorage for state
    cy.window().then((win) => {
      const userToken = win.localStorage.getItem('authToken');
      expect(userToken).to.exist;
    });
  });

  it('should limit API intercepts', () => {
    // Only intercept what's needed
    cy.intercept('POST', '/api/users', { statusCode: 201 }).as('createUser');
    
    cy.visit('https://example.com/users/create');
    cy.get('form').within(() => {
      cy.get('input[name="email"]').type('test@example.com');
      cy.get('button[type="submit"]').click();
    });
    
    cy.wait('@createUser');
  });
});
```

### 6. **Common Pitfalls to Avoid** ⚠️

```javascript
describe('Common Pitfalls & Solutions', () => {
  it('AVOID: Detached DOM elements', () => {
    // ❌ Element might be detached after re-render
    // const $element = cy.get('.item');
    // cy.wait(1000);
    // cy.wrap($element).click(); // Fails if DOM updated
    
    // ✅ Query fresh each time
    cy.get('.item').click();
  });

  it('AVOID: Mixed sync/async code', () => {
    cy.visit('https://example.com');
    
    // ✅ Chain Cypress commands
    cy.get('button').click();
    cy.url().should('include', '/page2');
    
    // ❌ Avoid mixing with setTimeout
    // setTimeout(() => {
    //   cy.get('input').type('text'); // Wrong!
    // }, 1000);
  });

  it('AVOID: Testing multiple things at once', () => {
    // ❌ Tests too much in one case
    // it('should do everything', () => {
    //   // Login, create user, edit user, delete user
    // });
    
    // ✅ Each test should have single responsibility
  });

  it('AVOID: Over-mocking network', () => {
    // ❌ Over-mocking makes tests less realistic
    // cy.intercept('GET', '/api/**', (req) => {
    //   req.reply({ status: 200, body: {} });
    // });
    
    // ✅ Mock only external dependencies
    cy.intercept('POST', '/api/auth', { statusCode: 200 }).as('auth');
    
    // Let actual endpoints work when possible
  });

  it('AVOID: Hardcoded test data', () => {
    // ❌ Hardcoded values
    // cy.get('input').type('test@example.com');
    // cy.get('input[name="password"]').type('Password123!');
    
    // ✅ Use fixtures or dynamic data
    cy.fixture('users').then((users) => {
      cy.get('input[name="email"]').type(users[0].email);
      cy.get('input[name="password"]').type(users[0].password);
    });
  });
});
```

### 7. **Debugging & Troubleshooting** 🔧

```javascript
describe('Debugging Techniques', () => {
  it('should use debug() for inspection', () => {
    cy.visit('https://example.com');
    
    cy.get('[data-testid="user-list"]')
      .debug() // Pauses execution, opens DevTools
      .find('.user-item')
      .first()
      .debug()
      .click();
  });

  it('should use log() for custom messages', () => {
    cy.visit('https://example.com');
    
    cy.log('Starting user creation');
    cy.get('button[data-action="create"]').click();
    
    cy.log('Filling form');
    cy.get('input[name="email"]').type('test@example.com');
    
    cy.log('Submitting form');
    cy.get('button[type="submit"]').click();
  });

  it('should inspect element properties', () => {
    cy.visit('https://example.com');
    
    cy.get('[data-testid="user-card"]').then(($element) => {
      // Log to console
      cy.log('Element HTML:', $element.html());
      cy.log('Element text:', $element.text());
      cy.log('Element classes:', $element.attr('class'));
      
      // Conditional debugging
      if ($element.hasClass('error')) {
        cy.log('ERROR class found!');
      }
    });
  });

  it('should use screenshot for visual debugging', () => {
    cy.visit('https://example.com');
    
    cy.screenshot('homepage'); // Auto-saves to cypress/screenshots
    
    cy.get('button').click();
    cy.screenshot('after-click');
  });

  it('should watch variables', () => {
    cy.visit('https://example.com');
    
    cy.window().then((win) => {
      // Access window variables
      cy.log('User:', win.currentUser);
      cy.log('Token:', win.authToken);
    });
  });
});
```

### 8. **Continuous Integration Tips** 🚀

```javascript
// cypress.config.js
module.exports = defineConfig({
  e2e: {
    // CI/CD optimizations
    baseUrl: 'http://localhost:3000',
    
    // Timeout configs
    defaultCommandTimeout: 10000,
    requestTimeout: 15000,
    
    // Screenshot & Video on failure
    screenshotOnRunFailure: true,
    video: true, // Record all runs
    
    // Retry failed tests
    retries: {
      runMode: 2, // Retry 2 times in CI
      openMode: 0 // No retry in interactive mode
    },
    
    // Parallel execution
    specPattern: 'cypress/e2e/**/*.cy.js'
  }
});

// Usage in CI/CD
describe('CI/CD Aware Tests', () => {
  it('should handle CI environment', () => {
    const isCI = Cypress.env('CI') === true;
    
    if (isCI) {
      // Different behavior for CI
      cy.log('Running in CI environment');
      cy.visit(Cypress.env('BASE_URL') || 'http://localhost:3000');
    } else {
      cy.visit('http://localhost:3000');
    }
  });

  it('should log environment info', () => {
    cy.log('Browser:', Cypress.browser.name);
    cy.log('Platform:', Cypress.platform);
    cy.log('Node Version:', Cypress.version);
  });
});
```

### Summary: Quick Reference Checklist

- ✅ Write independent, isolated tests
- ✅ Use explicit waits over hard waits
- ✅ Avoid brittle selectors (use data-testid)
- ✅ Handle errors and edge cases
- ✅ Use Page Object Model for organization
- ✅ Implement custom commands for reusability
- ✅ Mock external APIs, test real flows
- ✅ Use fixtures for test data
- ✅ Batch assertions for performance
- ✅ Debug with debug(), log(), and screenshots
- ✅ Set up proper CI/CD configuration
- ✅ Retry failed tests in CI pipelines

[⬆️ back to top](#table-of-contents)

---

## 📚 Learning Resources

### Official Documentation
- [Cypress Official Documentation](https://docs.cypress.io)
- [Cypress Best Practices](https://docs.cypress.io/guides/references/best-practices)
- [Cypress API Reference](https://docs.cypress.io/api/table-of-contents)

### Tutorials & Guides
- [CSS Selectors Guide](https://www.w3schools.com/cssref/selectors_class.asp)
- [XPath Tutorial](https://www.w3schools.com/xml/xpath_intro.asp)
- [Chai Assertion Library](https://www.chaijs.com/)
- [MDN Web Docs - DOM Selectors](https://developer.mozilla.org/en-US/docs/Web/API/Document_querySelector)

### Advanced Topics
- [Cypress Real World App](https://github.com/cypress-io/cypress-realworld-app)
- [Cypress Testing Library](https://testing-library.com/docs/cypress-testing-library/intro/)
- [Page Object Model Pattern](https://github.com/cypress-io/example-apps)

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/new-tests`)
3. Add your test cases or improvements
4. Commit your changes (`git commit -m 'Add new test cases'`)
5. Push to the branch (`git push origin feature/new-tests`)
6. Open a Pull Request

---

## 📝 License

This project is open source and available for educational purposes.

---

## 🎯 Goals & Learning Outcomes

By completing this framework, you will:

✅ Master Cypress fundamentals and advanced features  
✅ Understand various locator strategies and selector techniques  
✅ Learn best practices for writing scalable test automation  
✅ Develop skills in test organization and structure  
✅ Implement custom commands and reusable utilities  
✅ Handle complex UI interactions and validations  
✅ Create maintainable, robust test suites  
✅ Prepare for professional automation testing roles  

---

## 🚀 Next Steps

1. **Start with basics**: Review the Basic Usage Examples section
2. **Practice selectors**: Explore all Locator Strategies
3. **Implement POM**: Refactor tests using Page Object Model
4. **Learn advanced**: Study Custom Commands and Advanced Techniques
5. **Join community**: Share your tests and learn from others

---

**Last Updated**: May 2026  
**Author**: BrianGator  
**Status**: Active Development 🚀

---

## Quick Navigation Links

- [🔝 Back to Top](#cypress-automation-testing-framework-ninja-)
- [📋 Table of Contents](#table-of-contents)
- [💻 View Basic Examples](#basic-usage-examples)
- [🏗️ Learn Page Object Model](#page-object-model-pattern)
- [✅ Master Assertions](#assertions--validations-guide)
- [🔍 Explore Locators](#locator-strategies-comprehensive-guide)
- [📝 Read Best Practices](#cypress-best-practices--tips-guide)
