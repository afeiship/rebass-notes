# props
> All Rebass components extend the base Box component, and include Styled System props

## sx
> 与style不同之处在于，这里会优先找配置。
```jsx
<Box
  sx={{
    color: 'primary', // theme.colors.primary
    fontSize: 2,      // theme.fontSizes[2]
    margin: 3,        // theme.space[3]
  }}>
  Hello
</Box>

// 而且还支持 pesuade 
<Button
  sx={{
    ':hover': {
      backgroundColor: 'tomato',
    }
  }}>
  Beep
</Button>

// responsive
// example theme
export default {
  breakpoints: [ '40em', '52em', '64em' ],
}

<Box
  sx={{
    margin: [ 0, 1, 2 ],
  }}
/>

// 或者你也可以这样
<Box
  sx={{
    display: 'block',
    '@media screen and (max-width: 64em)': {
      display: 'none',
    }
  }}
/>
```

## box
~~~
m: margin
mt: margin-top
mr: margin-right
mb: margin-bottom
ml: margin-left
mx: margin-left and margin-right
my: margin-top and margin-bottom
p : padding
pt: padding-top
pr: padding-right
pb: padding-bottom
pl: padding-left
px: padding-left and padding-right
py: padding-top and padding-bottom
~~~

```jsx
// Numbers reference steps on the spacing scale
// e.g. 8px
<Text m={2} />
// Numbers greater than the length of `theme.space.length` are converted to pixels
<Text my={256} />
// Negative values can be used to add negative margins
<Text mx={-2} />
// Strings can be used for other values
<Text mx='auto' />
// Arrays can be used for mobile-first responsive styles
<Text m={[ 0, 1, 2 ]} />
```


## as
> The underlying HTML element rendered in any component can be overridden by the as prop.
```jsx
<Heading as='h1'>Hello</Heading>
```
