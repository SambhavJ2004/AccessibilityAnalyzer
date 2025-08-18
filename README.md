# Accessibility Analyzer Website

A web-based tool designed to perform on-demand accessibility audits of any website, helping developers identify and fix issues based on WCAG (Web Content Accessibility Guidelines) standards.

![Live Demo Screenshot]<img width="1903" height="679" alt="image" src="https://github.com/user-attachments/assets/17523105-d3b6-4679-a578-a97d9bdecf61" />




---

## Table of Contents

- [About The Project](#about-the-project)
- [How It Works](#how-it-works)
- [Built With](#built-with)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contact](#contact)

---

## About The Project

This project provides a simple yet powerful interface for developers and designers to quickly assess the accessibility of their web pages. By entering a URL, users can receive a detailed report of accessibility violations, presented in a clear and actionable format. The goal is to make accessibility testing a more integrated part of the web development workflow.

Key features include:
* **On-Demand Audits:** Analyze any live website by simply providing its URL.
* **Automated Analysis:** Leverages powerful tools to automatically scan a webpage's DOM for accessibility violations.
* **WCAG-Based Reporting:** Audits are performed against established WCAG standards to ensure comprehensive testing.
* **Dynamic Front-End:** A clean user interface allows users to initiate scans and view the resulting audit data in a formatted table.

---

## How It Works

The application uses a client-server architecture:

1.  **User Input:** The user submits a URL through the front-end interface built with HTML, CSS, and JavaScript.
2.  **Back-End Processing:** The Node.js and Express.js server receives the request.
3.  **Headless Browsing:** **Puppeteer** launches a headless instance of Chromium to navigate to the target URL.
4.  **Accessibility Scan:** Once the page is loaded, **axe-core** is injected into the page to perform the accessibility audit.
5.  **Results:** The audit results (a JSON object detailing violations) are sent back to the server.
6.  **Display:** The server forwards the results to the front-end, where they are dynamically rendered in a table for the user to review.

---

## Built With

This project utilizes a modern tech stack to deliver a fast and reliable user experience.

* **Back-End:**
    * [Node.js](https://nodejs.org/) - JavaScript Runtime Environment
    * [Express.js](https://expressjs.com/) - Web Framework for Node.js
* **Front-End:**
    * [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
    * [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS)
    * [JavaScript (ES6+)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* **Core Tools:**
    * [Puppeteer](https://pptr.dev/) - Headless Chrome Node.js API
    * [axe-core](https://github.com/dequelabs/axe-core) - Accessibility Testing Engine

---

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You must have Node.js and npm (Node Package Manager) installed on your machine.
* You can download Node.js [here](https://nodejs.org/).

### Installation

1.  **Clone the repository**
    ```sh
    git clone [https://github.com/SambhavJ2004/accessibility-checker.git](https://github.com/SambhavJ2004/accessibility-checker.git)
    ```
2.  **Navigate to the project directory**
    ```sh
    cd accessibility-checker
    ```
3.  **Install NPM packages**
    ```sh
    npm install
    ```
4.  **Start the server**
    ```sh
    npm start
    ```
    The application should now be running on `http://localhost:3000` (or the port specified in your server code).

---

## Usage

1.  Open your web browser and navigate to the application's URL (e.g., `http://localhost:3000`).
2.  Enter the full URL of the website you wish to analyze in the input field.
3.  Click the "Analyze" or "Scan" button.
4.  Wait for the audit to complete. The results will be displayed in the table below, showing any detected accessibility violations.

---

## License

Distributed under the MIT License. See `LICENSE` for more information.

---
