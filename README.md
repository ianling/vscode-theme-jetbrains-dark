# Visual Studio Code Theme: Jetbrains Dark

Intended to exactly replicate the syntax highlighting of Jetbrains Goland (as of 2024-11).

This theme only supports Go files because those are the only ones I care about syntax highlighting for.

## Known Limitations

- Neither TextMate highlighting nor semantic highlighting (via the Go language server, `gopls`) allow me to highlight words in comments if they match known types
- There is no way to highlight method receiver arguments
    - For example, `abc` is not specifically highlightable in: `func (abc *Type) Delete() error {...}`
        - It is also not highlightable within the function body
- There is no way to make `make()` blue while also making other built-ins like `append()` and `len()` orange
- There is no way to highlight variable names when they shadow names that are already used in the same scope
    - A common example: `if err := ...` will often cause `err` to be specifically highlighted in a different color when `err` is already initialized in the same scope
- There is no way to highlight `TODO` comments

## Changelog

- 2024-11-18
    - Updated colors to more closely match Goland using a color picker this time
