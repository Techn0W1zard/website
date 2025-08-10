# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the TechnoWizard company website - a modern, dark-themed corporate site built with Astro and TypeScript. The site showcases TechnoWizard LLC's software development services, with a focus on their flagship project Sorteo Club (a private lottery platform for Mexico).

## Development Commands

```bash
# Start development server at localhost:4321
npm run dev

# Build production site to ./dist/
npm run build

# Preview production build locally
npm run preview

# Install dependencies
npm install
```

## Architecture & Key Concepts

### Tech Stack
- **Astro 5** with TypeScript for static site generation
- **Tailwind CSS 4** with Vite plugin for styling
- **No JavaScript frameworks** - pure Astro components for optimal performance

### Design System
The site uses a consistent dark theme with defined color variables:
- Primary: Electric Blue (#0066FF)
- Secondary: Deep Purple (#6B46C1)  
- Accent: Cyan (#00D4FF)
- Background: Gray-950 with Gray-100 text

### Site Structure
- **Layout System**: Single base layout (`src/layouts/Layout.astro`) with TypeScript props interface
- **Navigation**: Fixed header with mobile-responsive hamburger menu (`src/components/Navigation.astro`)
- **Pages**: File-based routing with 5 main pages (Home, About, Services, Portfolio, Contact)
- **Styling**: Global CSS in `src/styles/global.css` with Tailwind base layer customizations

### Content Strategy
- **Homepage**: Hero section with animated backgrounds, services preview, CTA sections
- **About**: Company story, statistics, core values with icon grid
- **Services**: Detailed service offerings in card layout, development process timeline
- **Portfolio**: Featured project (Sorteo Club) with detailed case study, technology showcase
- **Contact**: Professional contact form with FAQ section and company info

### Typography & Fonts
- Display font: Space Grotesk (headings)
- Body font: Inter (paragraphs, UI)
- Fonts loaded via Google Fonts with preconnect optimization

### Component Patterns
- Gradient backgrounds and borders for visual hierarchy
- Consistent icon usage with Heroicons SVGs
- Hover effects and transitions for interactivity
- Mobile-first responsive design with Tailwind breakpoints

### Form Handling
The contact form uses client-side JavaScript for basic submission handling (currently simulated). For production, integrate with form handling services like Formspree or Netlify Forms.

## Content Updates

When updating content:
- Company information and service descriptions are in individual page files
- Color scheme variables are in `src/styles/global.css` 
- Navigation links are defined in the Navigation component
- SEO metadata (titles, descriptions) are passed as props to the Layout component