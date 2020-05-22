# theming

## theme-provider
```shell
npm i @rebass/preset emotion-theming
```

```jsx
import React from 'react'
import { ThemeProvider } from 'emotion-theming'
import theme from '@rebass/preset'
export default props =>
  <ThemeProvider theme={theme}>
    {props.children}
  </ThemeProvider>
```


## theme-ui
```jsx
import { ThemeProvider } from 'theme-ui'

import React from 'react'
import {
  Box,
  Card,
  Image,
  Heading,
  Text
} from 'rebass'
export default ({
  image,
  title,
  description
}) =>
  <Box width={256}>
    <Card
      sx={{
        p: 1,
        borderRadius: 2,
        boxShadow: '0 0 16px rgba(0, 0, 0, .25)',
      }}>
      <Image src={image} />
      <Box px={2}>
        <Heading as='h3'>
          {title}
        </Heading>
        <Text fontSize={0}>
          {description}
        </Text>
      </Box>
    </Card>
  </Box>
```

## theming
```jsx
import React from 'react'
import { ThemeProvider } from 'emotion-theming'
const theme = {
  fontSizes: [
    12, 14, 16, 24, 32, 48, 64
  ],
  colors: {
    primary: '#07c',
    gray: '#f6f6ff',
  },
  buttons: {
    primary: {
      color: 'white',
      bg: 'primary',
    },
    outline: {
      color: 'primary',
      bg: 'transparent',
      boxShadow: 'inset 0 0 0 2px'
    },
  },
}
export default props =>
  <ThemeProvider theme={theme}>
    {props.children}
  </ThemeProvider>
```
