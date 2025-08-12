# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML landing page for Grytte, Inc. - "The Educational Network" launching Summer 2025. The project is a single-page application showcasing educational networking features including industry organizations, professional certifications, workforce areas, training providers, schools/universities, and exam vouchers.

## Architecture

- **Single HTML file**: `index.html` contains all markup, styles, and JavaScript
- **Static asset structure**: All images organized in `/images/` with subfolders for different content types
- **No build system**: Direct HTML file that can be opened in browser or served statically
- **CSS Framework**: Uses Tailwind CSS via CDN (`@tailwindcss/browser@4`)
- **Custom Fonts**: Gilroy Light and ExtraBold fonts loaded from `/fonts/` directory

## Key Components

### Styling System
- Custom color scheme with CSS variables:
  - `#f0f0f0` (bg-main) - main background
  - `#304661` (text-main/bg-blue) - primary text and CTA buttons
  - `#D7DFED` (bg-cta) - call-to-action section background
  - `#4784d0` (border-blue) - selection borders
- Font hierarchy: Gilroy-extrabold for headings, Gilroy-light for body text

### Dynamic Content Loading
JavaScript functions in `index.html:334-491`:
- `loadImages()` - Dynamically loads image grids with click selection
- `loadAreas()` - Generates pill-style buttons for workforce areas
- Image categories: organizations (52), certifications (14), training (15), schools (14), vouchers (10)

### Content Sections
- Header with email signup form and hero image
- Industry Organizations showcase (1,600+)
- Professional Certifications grid (4,000+)  
- Workforce Areas pills (1,000+)
- Training Providers grid (300+)
- Schools/Universities grid (10,000+)
- Exam Vouchers grid (100+)
- Footer with contact information and social links

## Development Notes

Since this is a static HTML project:
- No package.json, build scripts, or dependencies
- Open `index.html` directly in browser for development
- All assets are relative paths from project root
- JavaScript is inline within the HTML file
- Responsive design using Tailwind CSS classes