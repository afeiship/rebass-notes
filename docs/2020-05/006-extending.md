# extending
> To extend a component, pass props through and define custom styles in the sx prop.

```jsx
import React from 'react'
import { Box } from 'rebass'
const Container = props =>
  <Box
    {...props}
    sx={{
      maxWidth: '1024px',
      mx: 'auto',
      px: 3,
    }}
  />
```

## short hand
```jsx
// If you're using CSS properties that have shorthand variations, try to use the normal CSS property instead.

// avoid shorthand syntax
sx={{
  border: '1px solid tomato',
}}
// use regular properties instead
sx={{
  borderWidth: '1px',
  borderStyle: 'solid',
  borderColor: 'tomato',
}}
```

## Default Variants
```js
variants: {
  badge: {
    color: 'white',
    bg: 'tomato',
    px: 2,
  },
}

const Badge = props =>
  <Box
    variant='badge'
    {...props}
  />
```
