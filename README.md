# 📦 ECM Marketplace App

## Overview

ECM Marketplace App is a minimal web application designed as an **Application Under Test (AUT)** for practicing UI automation.

The system simulates an e-commerce flow with authentication, product browsing, cart management, and checkout, using only client-side logic.

---

## Purpose

This application is designed to:

- Provide a controlled environment for UI test automation
- Simulate real-world frontend behaviors (async operations, state management)
- Enable practice with test synchronization, validation, and design patterns

---

## Architecture (High-Level)

The application is implemented as a static frontend:

```
HTML Pages + Inline JavaScript
        ↓
localStorage (state persistence)
        ↓
Simulated async operations (setTimeout)
```

### Key Characteristics

- No backend (fully client-side)
- State managed via `localStorage`
- Navigation through static HTML pages
- Intentional delays to simulate asynchronous behavior

---

## Features / Scope

The application supports:

- User authentication (success and failure scenarios)
- Product listing and search
- Add-to-cart functionality
- Cart persistence
- Checkout flow with validation

---

## Tech Stack

- HTML5
- Vanilla JavaScript
- CSS
- Node.js (optional local server)

---

## How It Works

### Authentication

- Valid login sets `localStorage.auth = "true"`
- Invalid login displays an error message
- Successful login triggers a delayed redirect to products page

### Products

- Product list stored in-memory
- Search implemented with debounce (~400ms delay)
- Cart stored as JSON in `localStorage`

### Checkout

- Reads cart from `localStorage`
- Validates authentication state
- Simulates processing delay (~500ms)
- Clears cart upon successful order

---

## Relationship with QA Automation Project

This repository is the **System Under Test (SUT)**.

👉 QA Automation Suite: https://github.com/lucaspc6/ecm-qa-automation

### Interaction Flow

```
ECM Marketplace App (SUT)
          ↑
QA Automation Suite
```

The QA project:

- Executes user flows
- Interacts with the UI
- Validates behavior and state
- Handles async operations through explicit waits

This separation reflects real-world QA engineering practices.

---

## Setup Instructions

### Option 1 — Node.js

```bash
npm install
npm start
```

Open:

```
http://localhost:8080
```

---

### Option 2 — Python

```bash
cd app
python3 -m http.server 8080
```

Open:

```
http://localhost:8080
```

---

## Notes for Reviewers

- Intentionally simple system focused on testability
- Includes async behavior and state management
- Designed to support UI test automation scenarios
- Paired with a dedicated automation project
