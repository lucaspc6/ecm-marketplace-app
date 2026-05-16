# ECM Marketplace - QA Automation Test App

A minimal web application designed for QA automation practice with Selenium, Playwright, or similar testing frameworks.

## Purpose

This application serves as an Application Under Test (AUT) for practicing UI automation. It includes:
- Intentional async delays to practice explicit waits
- localStorage-based authentication and cart management
- Stable element IDs for reliable test locators
- Multiple user flows for comprehensive test scenarios

## Project Structure

```
.
├── app/
│   ├── index.html      # Home page with navigation
│   ├── login.html      # Login page with authentication
│   ├── products.html   # Product catalog with search and cart
│   └── checkout.html   # Checkout page with order completion
├── server/
│   └── server.js       # Simple static HTTP server
├── package.json        # Project configuration
└── README.md          # This file
```

## How to Run

### Option 1: Node.js Server (Recommended)

1. Install dependencies (none required, but run for future compatibility):
   ```bash
   npm install
   ```

2. Start the server:
   ```bash
   npm start
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

### Option 2: Python Simple Server (Alternative)

1. Navigate to the app directory:
   ```bash
   cd app
   ```

2. Start Python's built-in HTTP server:
   ```bash
   python3 -m http.server 8080
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

