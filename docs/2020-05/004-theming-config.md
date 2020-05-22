# theming-config

```jsx
import React from 'react'
import theme from './theme'
import { ThemeProvider } from 'emotion-theming'
// or for use with Theme UI:
// import { ThemeProvider } from 'theme-ui'
export default props =>
  <ThemeProvider theme={theme}>
    {props.children}
  </ThemeProvider>
```


## config
```jsx
// example theme.js
export default {
  breakpoints: ['40em', '52em', '64em'],
  fontSizes: [
    12, 14, 16, 20, 24, 32, 48, 64
  ],
  colors: {
    blue: '#07c',
    lightgray: '#f6f6ff'
  },
  space: [
    0, 4, 8, 16, 32, 64, 128, 256
  ],
  fonts: {
    body: 'system-ui, sans-serif',
    heading: 'inherit',
    monospace: 'Menlo, monospace',
  },
  fontWeights: {
    body: 400,
    heading: 700,
    bold: 700,
  },
  lineHeights: {
    body: 1.5,
    heading: 1.25,
  },
  shadows: {
    small: '0 0 4px rgba(0, 0, 0, .125)',
    large: '0 0 24px rgba(0, 0, 0, .125)'
  },
  variants: {
  },
  text: {
  },
  buttons: {
    primary: {
      color: 'white',
      bg: 'primary',
    }
  }
}
```


## usage
```jsx
<ThemeProvider
  theme={{
    colors: {
      background: 'black',
      primary: 'tomato',
    },
    space: [ 0, 6, 12, 24, 48 ],
    fontSizes: [ 14, 16, 18, 20, 24 ],
    radii: {
      default: 12,
    }
  }}>
  <Button>Beep</Button>
</ThemeProvider>
```
