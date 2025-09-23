# TypeScript Configurations

A collection of reusable TypeScript configuration files for different project types.

## Overview

This repository contains shared TypeScript configurations that can be extended in your projects. It helps maintain consistency across multiple projects by centralizing the TypeScript settings.

## Available Configurations

### Base Configuration (`base.json`)

The foundational TypeScript configuration that other configs extend from. It includes:

- Strict type checking options
- Modern JavaScript/ESNext features
- ES Modules interop
- DOM and DOM.Iterable libraries
- Skip lib checks for faster compilation

### Next.js Configuration (`nextjs.json`)

Specific configuration for Next.js projects that extends the base configuration with:

- Next.js plugin support
- JSX preservation for Next.js
- Module resolution set to Bundler
- JavaScript file allowance

### React Library Configuration (`react-library.json`)

Configuration for React component libraries that extends the base configuration with:

- React JSX transformation

## Installation

```bash
npm install @repo/typescript-config
```

## Usage

Extend the appropriate configuration in your project's `tsconfig.json`:

### For general projects

```json
{
  "extends": "@repo/typescript-config/base.json"
}
```

### For Next.js projects

```json
{
  "extends": "@repo/typescript-config/nextjs.json"
}
```

### For React libraries

```json
{
  "extends": "@repo/typescript-config/react-library.json"
}
```

## Configuration Details

### Base Configuration Options

- `declaration`: Generates corresponding `.d.ts` files
- `declarationMap`: Generates sourcemaps for declaration files
- `esModuleInterop`: Enables emit interoperability between CommonJS and ES Modules
- `isolatedModules`: Ensures each file can be safely transpiled without relying on other imports
- `lib`: Specifies library files to be included in the compilation
- `module`: Sets the module system to NodeNext
- `moduleDetection`: Forces module detection
- `moduleResolution`: Sets the module resolution strategy to NodeNext
- `noUncheckedIndexedAccess`: Adds `undefined` to a `T` when accessing arrays and objects
- `resolveJsonModule`: Allows importing `.json` files
- `skipLibCheck`: Skips type checking of declaration files
- `strict`: Enables all strict type checking options
- `target`: Sets the JavaScript language version for emitted JavaScript
