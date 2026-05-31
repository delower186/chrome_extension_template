# Chrome Extension Template

A modern, scalable, and production-ready Chrome Extension Development Template built by Sandalia Apps. This template provides a clean project structure, Manifest V3 support, Bootstrap integration, and best practices for building secure and maintainable browser extensions.

## Features

- Manifest V3 Ready
- Modern Project Structure
- Popup UI Support
- Content Scripts Support
- Background Service Worker
- Options Page Support
- Bootstrap Integration (Local Assets)
- Chrome Storage API
- Messaging Between Components
- Secure Content Security Policy (CSP)
- Easy Customization
- Production-Ready Setup

## Project Structure

```text
chrome-extension-template/
│
├── manifest.json
├── pages/
│   └── index.html
│
├── background/
│   └── service-worker.js
│
├── content/
│   └── content.js
│
└── assets/
   ├── css/
   |   |── bootstrap.min.css
   │   └── style.css
   ├── js/
   |   |── bootstrap.bundle.min.js
   │   └── main.js
   └── images/ icons/
        ├── default_icon.png
        ├── icon16.png
        ├── icon32.png
        ├── icon48.png
        └── icon128.png

```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/delower186/chrome_extension_template.git
```

### 2. Customize Extension Information

Update the following fields in `manifest.json`:

```json
{
  "name": "My Chrome Extension",
  "description": "Extension description",
  "version": "1.0.0"
}
```

### 3. Load the Extension

1. Open Chrome
2. Navigate to:

```text
chrome://extensions/
```

3. Enable **Developer Mode**
4. Click **Load Unpacked**
5. Select the project directory

## Bootstrap Integration

Chrome Extensions do not allow remote JavaScript execution from CDNs. Therefore, Bootstrap assets should be bundled locally.

Example:

```html
<link rel="stylesheet" href="assets/css/bootstrap.min.css">
<script src="assets/js/bootstrap.bundle.min.js"></script>
```

## Manifest V3 Example

```json
{
    "manifest_version":3,
    "name":"extension_name",
    "version":"1.0",
    "description":"Chrome Extension Description",
    "action":{
        "default_popup":"pages/index.html",
        "default_icon": "images/icons/default_icon.png"
    },
    "icons": {
        "16": "images/icons/icon16.png",
        "32": "images/icons/icon32.png",
        "48": "images/icons/icon48.png",
        "128": "images/icons/icon128.png"
    },
    "permissions":[
        "storage",
        "tabs"
    ],
    "content_scripts":[
        {
            "matches":["<all_urls>"],
            "js":["js/content.js"]
        }
    ],
    "background":{
        "service_worker": "js/service-worker.js"
    }
}
```

## Chrome APIs Included

This template is designed to work with:

- `chrome.storage`
- `chrome.tabs`
- `chrome.runtime`
- `chrome.scripting`
- `chrome.notifications`
- `chrome.contextMenus`
- `chrome.action`

## Security Best Practices

- Use Manifest V3
- Bundle all JavaScript locally
- Avoid inline scripts
- Minimize permissions
- Validate all external data
- Follow Chrome Web Store policies

## Development Workflow

1. Make changes to the source files
2. Reload the extension from Chrome Extensions page
3. Test functionality
4. Build and package for release

## Browser Compatibility

- Google Chrome
- Microsoft Edge
- Brave Browser
- Opera
- Chromium-based browsers

## Use Cases

- Web Automation Extensions
- Productivity Tools
- Data Extraction Extensions
- Form Fillers
- SEO Tools
- QA Testing Utilities
- Developer Productivity Extensions
- AI-Powered Browser Tools

## About Sandalia Apps

Sandalia Apps specializes in developing high-quality applications, automation solutions, browser extensions, web platforms, and QA automation frameworks. Our focus is on creating scalable, maintainable, and user-friendly software solutions for businesses and individuals.

## License

MIT License

Copyright (c) Sandalia Apps

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files to deal in the Software without restriction.