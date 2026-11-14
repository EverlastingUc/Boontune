# Boontune

**Boontune** is an original, experimental interpreted programming language implemented in dependency-free JavaScript.

> Early development · 0.1.0

## Example

```boon
tune greeting = "Hello from Boontune"
tune name = "world"
play greeting + ", " + name + "!"

tune score = 7
set score = score * 2
if (score >= 14) {
  play "Level reached."
} else {
  play "Keep going."
}
```

## Syntax

- `tune name = expression` declares a variable.
- `set name = expression` updates an existing variable.
- `play expression` prints a value.
- `if (condition) { ... } else { ... }` selects a branch.
- Values: numbers, strings, `true`, `false`.
- Operators: arithmetic, comparisons, `and`, `or`, `not`.
- `#` begins a line comment; statements are newline-separated.

## Run

Requires Node.js 20+.

```sh
npm test
node src/cli.js examples/hello.boon
```

## Internals

Lexer → parser → abstract syntax tree → scoped environment → interpreter.

## Roadmap

- [x] Lexer and parser
- [x] Variables and expressions
- [x] Output and conditionals
- [x] Block scope
- [x] Initial automated tests
- [ ] Functions and return values
- [ ] Loops and collections
- [ ] Standard library and REPL
- [ ] Formal language specification

## License

MIT
