# variants

```jsx
// example theme with variants
export default {
  colors: {
    text: 'black',
    background: 'white',
    primary: 'tomato',
  },
  shadows: {
    card: '0 0 4px rgba(0, 0, 0, 0.125)',
  },
  variants: {
    card: {
      p: 2,
      bg: 'background',
      boxShadow: 'card',
      borderRadius: 2,
    },
    badge: {
      display: 'inline-block',
      p: 1,
      color: 'white',
      bg: 'primary',
      borderRadius: 2,
    }
  },
}

<Box variant='card' width={256}>
  Card
  <Box variant='badge'>
    Badge
  </Box>
</Box>

// example variant with dot notation
<Box variant='some.deeply.nested.object' />
```

## ideas
```jsx
theme.variants('$m.views.Button',{
  display:'inline-block',
  p: 2
});
```
