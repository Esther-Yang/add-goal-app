# Add Goal App

A React App that can add and delete goals, built while learning React.

# Feature

- A form that can input goal.
- Click the goal item to delete them.

# Ways to style React components

## CSS

- Dynamic inline styles using conditionals and states. The CSS in JS is written in camelCase.

```
<input style={ {borderColor : !isValid ? "red" : "#ccc" } }>
```

- Dynamic CSS Classes with template literals (`` ` ``). Inside the template literals, there are conditionals and states.

```
//CSS
.form-constol.invalid
```

```
//JS
<   className={ `form-control ${isValid? "invalid" : " "}`}>
```

## Styled Components

- Install styled component package.

```
npm install --save styled-components
```

- Import `styled`.

```
import styled from "styled-components";
```

- Use `styled`.

```
const Button = styled.button`
    //CSS here
`;
```

## CSS Modules

- Import (Convention to name it as `styles` or `classes`)

```
import styles from "./Button.module.css";
```

- Use

```
<button className={styles.button} >
<button className={styles['form-control']} >
```

# Summary

| Method            | Scope | Class Name                                                               |
| :---------------- | :---: | :----------------------------------------------------------------------- |
| CSS               |  ❌   | need to set unique class name by ourselves                               |
| Styled Components |   ✔   | generate unique string (E.g. xxx_xxx_xxx)                                |
| CSS Modules       |   ✔   | generate unique string in the form of ComponentName_CSSFile_UniqueString |
