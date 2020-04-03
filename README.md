# CSS transition livecode

The screencast: https://drive.google.com/file/d/1rp79SvN3y_zyfuq6KirSYac0mz0JqnFN/view?usp=sharing

Class 36, Fri Apr 3 2020

```
CSS
- selectors
- devtools
- flexbox
- transitionable properties
- using react

css
  :hover pseudoclass
  transform: ??;
  text-decoration: underline;
  color: black;
  font-weight: bold;

1. CSS transitions <-
2. CSS animations
3. animating css properties with JS
```

CSS fundamentals:

- external / inline

- selectors

  - by class: .my-class-name <- use these
  - by id (identifier): #nav
  - by type/tag: ul
  - by pseudoclass :hover, :active, etc.

- combine selectors:

  - select (deeply nested) children

    ```css
    .menu a {
      // ..
    }
    ```

  - select on multiple criteria together

    ```css
    button.primary {
      // ..
    }
    ```

- specificity

- if you have different _states_ that an element can be in

```css
a {
  color: red;
  transition: all 0.5s ease;
}

a:hover {
  color: black;
}
```

- DevTools are _really_ powerful
  - use them to reverse engineer
  - use them to play around with your own styles while developing

React?

- routing, usestate
- props/state
- dev server
  - `const [open, set_open] = useState(false);`
  - ```
    <div className={open ? "menu open" : "menu"}>...</div>
    ```
  - ```css
    .menu {
      color: "red";
      transition: color 0.2s ease;
    }
    .menu.open {
      color: "black";
    }
    ```
- consitionally set styles directly

  - `const [open, set_open] = useState(false);`
  - ```
    <div style={{ color: open ? "black" : "red", transition: "color .2s ease" }}>
      ...
    </div>
    ```

- CSS animations -> transition, multiple of them after each other
