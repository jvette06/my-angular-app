# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Essential Commands

**Development:**
- `npm start` or `ng serve` - Start development server on http://localhost:4200
- `ng build --watch --configuration development` - Build in watch mode for development

**Testing:**
- `ng test` - Run unit tests with Karma
- `ng test --watch=false` - Run tests once without watch mode

**Build:**
- `ng build` - Build for production (outputs to `dist/`)
- `ng build --configuration development` - Build for development

**Code Generation:**
- `ng generate component <name>` - Generate new component
- `ng generate service <name>` - Generate new service
- `ng generate module <name>` - Generate new module
- `ng generate directive|pipe|guard|interface <name>` - Generate other Angular schematics

## Architecture Overview

This is an Angular 17 application using standalone components architecture:

**Key Files:**
- `src/main.ts` - Application bootstrap
- `src/app/app.config.ts` - Application configuration with providers
- `src/app/app.routes.ts` - Routing configuration
- `src/app/app.component.ts` - Root component

**Project Structure:**
- Uses standalone components (no NgModules required)
- Routing configured through `provideRouter()` in app.config.ts
- TypeScript strict mode enabled
- Karma + Jasmine for testing

**Build Configuration:**
- Production builds use optimization and output hashing
- Development builds preserve source maps and disable optimization
- Bundle size limits: 500kb warning, 1mb error for initial bundles

**UI Framework:**
- Bootstrap 5.3.7 is configured and available globally
- Bootstrap CSS is loaded via angular.json styles configuration
- Use Bootstrap classes directly in component templates