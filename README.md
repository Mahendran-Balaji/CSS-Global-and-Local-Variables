# CSS-Global-and-Local-Variables

1) CSS variables can have a global or local scope.
2) To create a variable with global scope, declare it inside the :root selector. The :root selector matches the document's root element.
3) To create a variable with local scope, declare it inside the selector
4) Global Variable
```css
:root {
    --blue: #1e90ff;
    --white: #ffffff;
}
```
5) Access Global Variables using var()

Advantage of using var() : makes the code easier to read (more understandable)

```css
button {
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}
```
6) Override Global Variable With Local Variable
```css
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}
button {
    --blue: #0000ff; /* local variable will override global */
    background-color: var(--white);
    color: var(--blue);
    border: 1px solid var(--blue);
    padding: 5px;
}
```
7) Add a New Local Variable
```css
button {
  --button-blue: #0000ff; /* new local variable */
  background-color: var(--white);
  color: var(--button-blue);
  border: 1px solid var(--button-blue);
  padding: 5px;
}
```
8) Browser Support
   ```html
    Chrome: 49.0, IE: 15.0, Firefox: 31.0, Safari: 9.1, Opera: 36.0
   ```