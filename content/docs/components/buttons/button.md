# Button

The `<Button />` component is a versatile and fully customizable button component. It provides control over several aspects of styling, such as color, width, height, border, padding, margin, and more. It can be easily adapted to suit a variety of styles and use-cases.

<!--more-->

## Quick Sample Code

```jsx
import {Button} from 'solid-ui-shasta'

function App() {
  return <Button text="Hello" onClick={() => console.log('Clicked!')} />
}
```


## Props

Here is a list of all the props that the `Button` component accepts:

| Prop | Type | Description |
| --- | --- | --- |
| `children` | JSX.Element or JSX.Element[] | The content to be rendered inside the button. |
| `onClick` | function | Handler to be invoked when the button is clicked. |
| `ref` | function | Ref callback for the button. |
| `disabled` | boolean | If `true`, the button will be disabled. |
| `color` | string | The color of the button text. |
| `bgColor` | string | The background color of the button. |
| `width` | string | The width of the button. |
| `height` | string | The height of the button. |
| `borderRadius` | string | The border radius of the button. |
| `borderColor` | string | The color of the button border. |
| `border` | string | The border of the button. |
| `borderHover` | string | The border of the button on hover. |
| `padding` | string | The padding inside the button. |
| `margin` | string | The margin outside the button. |
| `key` | string | The key for the button. |
| `noActive` | boolean | If `true`, no active transformation will occur. |
| `boxShadowHover` | string | The box shadow of the button on hover. |
| `text` | string | The text to be rendered inside the button. |
| `gap` | string | The gap between the elements in the `Row` component. |
| `circle` | boolean | If `true`, the button will be styled as a circle. |
| `rounded` | string | The border radius when not a circle. |

## More Samples

Here's an example of how to use the `Button` component:


### Disabled button
Enable the disabled attribute for the button. This will prevent click event from being fired.
```jsx
<Button text="Hello" disabled />
```

### Styled button
This code will render a customized yellow button with the text "Hello" in white, and without a border either in default or hover state.
```jsx
<Button
  text="Hello"
  color={Color.white}
  bgColor="#FFBF00"
  border="0"
  borderHover="0"
/>
```

### Complex button
This provided JSX snippet exhibits the implementation of the `Button`, `Icon`, and `Text` components to construct an advanced button layout.
```jsx
import {Button, Color, Icon, Text} from 'solid-ui-shasta'

<Button border={`'1px solid' #${Color.pink2}`}>
  <Icon icon="iconoir-log-in" color={Color.pink2} />
  <Text color={Color.pink2}>Log In</Text>
</Button>
```

- The `Button` is being styled with a solid pink border using the `border` prop. The border color is obtained from the `Color` object, specifically `Color.pink2`.
- Inside this `Button` component, two child components are nested: `Icon` and `Text`.
- The `Icon` component displays a log-in icon specified by the `icon` prop. Its color is also set to pink (`Color.pink2`).
- The `Text` component renders the string "Log In" and, similar to the `Icon`, its color is set to pink (`Color.pink2`).

Essentially, this code creates a button with a pink border, which contains a log-in icon and text, both in matching pink color.



## CSS

The `Button` component uses CSS variables for styling. Here's a brief description of each variable:

- `--button-color`: The color of the button text.
- `--button-background-color`: The background color of the button.
- `--button-border-color`: The color of the button border.
- `--button-border-color-hover`: The color of the button border on hover.
- `--button-width`: The width of the button.
- `--button-height`: The height of the button.
- `--elevation-ground-box-shadow`: The box shadow of the button in its normal state.
- `--elevation-moderate-box-shadow`: The box shadow of the button on hover.
- `--color-disabled`: The color of the text when the button is disabled.
- `--background-color-disabled`: The background color of the button when it's disabled.
- `--filters-disabled`: The filter to apply when the button is disabled.
- `--button-padding`: The padding inside the button.
- `--button-margin`: The margin outside the button.

Remember to set these variables in your project's root stylesheet, or provide them directly as inline styles in the `Button` component. Failing to do so will result in the default browser styles being applied.

### Overriding CSS Variables
CSS variables can be overridden in your application by simply declaring them with new values in your CSS files. This is particularly useful if you want to apply custom themes or styles to the Button component.

For example, if you want to change the default color, background color, and border color for buttons across your app, you can add the following to your CSS:
```css
:root {
  --button-color: #color1;
  --button-background-color: #color2;
  --button-border-color: #color3;
}
```
Just replace `#color1`, `#color2`, and `#color3` with the color values you prefer. If you're using CSS modules or a similar scoped CSS system, be sure to define these variables in a global scope.
