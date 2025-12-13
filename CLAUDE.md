# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Timmerfabriek Sint Nyk website built with Astro 5.

## Commands

- `npm run dev` - Start development server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run preview` - Preview production build locally

## Architecture

### CSS Design System

All styles use a custom CSS design system with CSS custom properties (variables). Files are located in `src/styles/`:

- **global.css** - CSS reset and imports all other style files
- **colors.css** - Color palette variables (green, blue, dark-blue, gray scales 100-900)
- **typography.css** - Font family (Space Grotesk), weights, and responsive heading styles (H1-H5, paragraph)
- **spacing.css** - Spacing scale variables (0-1920px in rem)
- **container.css** - Reusable `.container` class with responsive padding and max-width

### Design Tokens

- Font: Space Grotesk (loaded via Google Fonts)
- Breakpoint: 1024px for desktop styles
- Mobile-first approach for all responsive styles

### Usage

Import `global.css` in Astro pages/layouts to access all design tokens:
```astro
import '../styles/global.css';
```

Use variables like:
```css
color: var(--green-500);
padding: var(--spacing-32);
font-weight: var(--font-semibold);
```
