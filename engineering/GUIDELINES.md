# Coding Guidelines

Apply these rules when generating or editing code. Keep output compact, but do not skip required documentation.

## Language-Agnostic Guidelines

- Add inline comments before non-trivial logical blocks so a reader can only skim the comments and understand the flow.
- Prefer self-explanatory code. Add comments only when they improve scanability or preserve intent.
- Comments should explain the `why`. Explain the `what` when the logic is non-obvious, algorithmic, or otherwise hard to infer from the code.
- Every `TODO` or `FIXME` must say exactly what needs to change or be fixed. Issue links are optional.
- Add a file-level header comment describing the file's responsibility.
- Prefer a `README.md` in major feature or domain directories to explain the module's purpose and architecture.
- Add an inline comment for magic numbers and complex regular expressions unless their purpose is obvious. Extracting them into named constants is preferred (not required).

## Language-Specific Guidelines

## JavaScript / TypeScript

- Use JSDoc/TSDoc for all functions.
- Include `@param` and `@returns` on every function. (can be omitted if the signature already makes them explicit)
- Include `@throws` only for custom or business-logic exceptions. Do not document standard built-in errors unless the code relies on them as part of the API contract.
- Add property or member comments only when the name does not already make the purpose clear.
- Include `@example` when usage is not obvious, especially for utilities or dense business logic.
- Include `@deprecated` for deprecated code and name the replacement or migration path.
- For `interface`, `type`, and `enum` declarations, add a doc comment on the declaration itself.
