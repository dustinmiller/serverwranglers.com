# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for "Server Wranglers" - a company offering premium managed server services. The project consists of a single-page HTML website that showcases enterprise server management services.

## Architecture

- **Static HTML Website**: Single `index.html` file containing all content
- **CSS Styling**: Complete `styles.css` with dark theme using CSS custom properties and responsive design
- **External Dependencies**: 
  - Font Awesome icons (CDN)
  - Google Fonts (Inter)
  - Missing: `script.js` for interactive functionality

## Styling System

The `styles.css` uses a dark theme with CSS custom properties:
- Primary colors: Dark purple/blue theme (`--bg-primary: #282a36`)
- Accent colors: Purple (`--accent-primary: #bd93f9`) and cyan (`--accent-cyan: #8be9fd`)
- Responsive design with mobile-first approach
- Animations for server rack visualization and hover effects

## Missing Files

The HTML references `script.js` which doesn't exist yet:
- `script.js` - JavaScript for mobile navigation toggle, contact form handling, and interactive animations

## Development

This is a basic static website project. No build tools, package managers, or frameworks are currently configured.

To add interactivity, create `script.js` to handle:
- Mobile hamburger menu toggle
- Contact form submission
- Smooth scrolling for navigation links
- Server animation enhancements