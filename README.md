# Node Farm

A simple Node.js application that displays farm products with detailed information in a clean, responsive interface.

## Description

Node Farm is a lightweight web application built with vanilla Node.js (no Express framework) that showcases various farm products. The application demonstrates fundamental Node.js concepts including:

- File system operations
- HTTP server creation
- Routing
- Template rendering
- Data handling with JSON

## Features

- Overview page with product cards
- Detailed product pages
- Simple API endpoint
- Slugified URLs
- Template-based HTML rendering

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/node-farm.git
   cd node-farm
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the application:
   ```
   npm start
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:3001
   ```

## Project Structure

```
node-farm/
│
├── index.js                  # Main application file
├── package.json              # Project metadata and dependencies
├── package-lock.json         # Locked dependencies
│
├── modules/
│   └── replaceTemplate.js    # Template replacement utility
│
├── templates/
│   ├── template-card.html    # Product card template
│   ├── template-overview.html# Overview page template
│   └── template-product.html # Product detail page template
│
└── dev-data/
    └── data.json             # Product data
```

## How It Works

The application uses a simple template system to render HTML pages. It reads HTML templates from files and replaces placeholders (like `{%PRODUCTNAME%}`) with actual data from the JSON file.

### Routes

- `/` or `/overview` - Shows the list of all products
- `/product?id=x` - Shows detailed information for a specific product
- `/api` - Returns the raw JSON data

## Dependencies

- [slugify](https://www.npmjs.com/package/slugify) (^1.6.6) - Used to create URL-friendly slugs from product names

## Development

This project uses nodemon for automatic server restarts during development. Make changes to the code and the server will automatically restart.

```
npm start
```

## Future Improvements

- Add a shopping cart functionality
- Implement user authentication
- Add payment processing
- Create an admin interface for product management
- Add search and filter capabilities
