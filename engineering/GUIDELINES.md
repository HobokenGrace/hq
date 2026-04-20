# Documentation and Readability Guidelines

This document outlines the standards for documentation and code readability across our JavaScript and TypeScript projects.

## 1. General Readability & Inline Comments

* **Block Summaries:** Use inline comments before logical blocks of code so readers can skim the comments to grasp what the entire block is doing without reading every line.
* **Business Logic (The "Why" and "What"):** Comments should emphasize the "why" to provide business context. For complex algorithms or unintuitive implementation details, explain the "what" alongside it.
* **Magic Numbers and Regular Expressions:** Place inline comments directly next to "magic numbers" (hardcoded values) and complex regular expressions explaining their specific purpose. Extracting them into constants is encouraged but not strictly required.
* **TODOs and FIXMEs:** Issue tracker links are not required, but you must include a detailed description of what needs to be done or fixed for easier future reference.

    ```typescript
    // TODO: Refactor the pagination calculation to handle edge cases where total items are less than the page size.
    ```

## 2. File and Directory Documentation

* **File-Level Comments:** A block comment is required at the top of every file explaining its overall purpose and contents.
* **Directory-Level Documentation:** Adding a `README.md` file is preferred, though not strictly required, in major feature or domain directories to explain the module's overarching architecture and purpose.

## 3. Function Documentation

* **JSDoc/TSDoc Requirement:** Use JSDoc/TSDoc to document all functions.
* **Parameters and Returns:** The `@param` and `@returns` tags are required for all functions to explain their purpose. However, you can omit explicit type annotations within the JSDoc tags if the TypeScript types are already explicit.
* **Exceptions:** Use the `@throws` tag to document custom or business-logic exceptions. You do not need to document standard built-in errors.
* **Examples:** Use `@example` tags for utility functions or complex business logic where the usage is not immediately obvious.
* **Deprecations:** Use the `@deprecated` tag for outdated code. You must include an explanation of the alternative solution or what to use instead. A strict removal timeline is not required.

## 4. TypeScript Types and Declarations

* **Type vs. Interface:** There is no strict preference between using `interface` or `type`. Use whichever fits the immediate context best (e.g., `interface` for standard object shapes, `type` for unions/intersections).
* **Documenting Declarations:** JSDoc comments are required for the `interface`, `type`, or `enum` declaration itself. You only need to add comments to individual properties or members if their purpose is not obvious from the name.
