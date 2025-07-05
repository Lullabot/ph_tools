# Placeholder Tools

Useful tools to share across Placeholder projects.

## Overview

The `ph_tools` module provides utility services and helper classes designed to simplify common development tasks across Placeholder Drupal projects. The module aims to provide robust, reusable components that handle edge cases and follow modern PHP and Drupal best practices.

## Features

- **Page Service**: Robust entity extraction from current route context
- **Exception Handling**: Custom exception classes for better error handling

## Architecture

### PageService

The `PageService` class provides methods to reliably extract entities from the current route context.

#### Key Methods

- `getNodeFromCurrentRoute()`: Specifically extracts node entities from the current route
- `getEntityFromCurrentRoute()`: Generic method for extracting any entity type from the current route

#### Supported Route Contexts

The PageService handles multiple route contexts:

1. **Standard Entity Routes**: Routes with automatically upcasted entity parameters
2. **Preview Routes**: Entity preview pages (e.g., `node_preview`)
3. **Revision Routes**: Entity revision pages with revision ID parameters
4. **UUID Routes**: Routes that reference entities by UUID

### Exception Handling

The module includes custom exception classes for better error handling:

- `InvalidContextException`: Thrown when the route context is invalid for entity extraction

## Future Enhancements

- **Hook System**: Convert entity parameter detection into a plugin/hook system
