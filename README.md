# Wilderness React

[Wilderness](https://github.com/colinmeinke/wilderness)
for [React](https://github.com/facebook/react).

Coming soon ...

## `<SVG>` component

### Syntax

```jsx
<SVG props={ props } />
```

## `<Shape />` component

### Syntax

```jsx
<SVG>
  <Shape props={ position1 }>
    <Shape props={ position2 } />
    <Shape props={ position3 } />
  </Shape>
</SVG>
```

## `<Play />` component

### Syntax

```jsx
<SVG>
  <Play props={ options }>
    <Shape name={ name }>
      <Shape />
      <Shape />
    </Shape>
    <Shape queue={ queue }>
      <Shape />
      <Shape />
    </Shape>
  </Play>
</SVG>
```

## Morph example

```jsx
import { SVG, Play, Shape } from 'react-wilderness';

const Triangle = () => (
  <Shape
    type="path"
    d="M40,90l30,20h-60z"
    fill="#E54"
  />
);

const Square = () => (
  <Shape
    type="rect"
    x={ 400 }
    y={ 100 }
    width={ 50 }
    height={ 50 }
    fill="#0FA"
  />
);

const Animation = () => (
  <Triangle>
    <Square />
  </Triangle>
);

const Morph = () => (
  <SVG>
    <Play
      duration={ 1800 }
      playing={ true }
    >
      <Animation />
    </Play>
  </SVG>
);

export default Morph;
```
