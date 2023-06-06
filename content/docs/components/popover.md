# `<Popover />`

The Popover component is a highly adaptable and customizable tooltip component for Solid.js applications. It provides a variety of styling options as well as functional versatility such as dynamically changing its position based on viewport dimensions.

## Quick Sample Code

```jsx
import { Popover, Text, Button } from "solid-ui-shasta";

function App() {
  return (
    <Popover
      padding="1rem"
      content={<Text>Hello</Text>}
    >
      <Button>Click Me</Button>
    </Popover>
  );
}
```

## Props

Below is a list of all the props that the `Popover` component accepts:

| Prop          | Type                         | Description                                                                                                                             |
| ------------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `children`    | JSX.Element or JSX.Element[] | The interactive content triggering the popover.                                                                                         |
| `position`    | string                       | The position of the popover relative to its triggering content. Possible values: 'top', 'bottom', 'left', 'right'. Default is 'bottom'. |
| `content`     | JSX.Element                  | The content to be displayed inside the popover.                                                                                         |
| `customStyle` | CSSProperties                | Custom styles to apply to the popover.                                                                                                  |
| `width`       | string                       | The width of the popover.                                                                                                               |
| `key`         | string                       | The key for the popover.                                                                                                                |

## More Samples

Here are some examples of how to use the `Popover` component:

### Popover with custom width

This example demonstrates how to customize the width of the Popover.

```jsx
<Popover position="top" width="300px" content={<div>Popover Content</div>}>
  <button>Trigger</button>
</Popover>
```

### Popover with custom styling

This example demonstrates how to add custom styles to the Popover.

```jsx
const customStyle = `
  backgroundColor: #8CB2D1;
  border: 1px solid #8CB2D1;
  borderRadius: 4px;
  padding: 1rem;
`
<Popover padding="1rem" content={<Text>Hello</Text>} customStyle={customStyle}>
  Click Me
</Popover>
```

### Popover with complex components

When the button labelled **Click Me** is clicked, a popover menu appears on the **left**. The menu includes the options `About`, `Open`, `Setting ...`, and `Exit`. The `Open` and `Setting ...` options also feature icons. Clicking on any menu item triggers the **callback** function.

```jsx
<Popover
  content={
    <Menu width="200px">
      <MenuItem key="about" onClick={callback}>
        <Text weight="200">About</Text>
      </MenuItem>
      <MenuDivider />
      <MenuItem key="open" onClick={callback}>
        <Row width="100%" justifyContent="space-between">
          <Text weight="200">Open</Text>
          <Icon icon="iconoir-open-new-window" />
        </Row>
      </MenuItem>
      <MenuItem key="settings" onClick={callback}>
        <Row width="100%" justifyContent="space-between">
          <Text weight="200">Setting ...</Text>
          <Icon icon="iconoir-settings" />
        </Row>
      </MenuItem>
      <MenuDivider />
      <MenuItem key="exit" onClick={callback}>
        <Text weight="200">Exit</Text>
      </MenuItem>
    </Menu>
  }
  position="left"
>
  <Button>Click Me</Button>
</Popover>
```

## CSS

The `Popover` component uses CSS variables for styling. Here's a brief description of each variable:

- `--popover-color`: The color of the Popover text.
- `--popover-background-color`: The background color of the Popover.
- `--popover-border-color`: The color of the Popover border.
- `--popover-width`: The width of the Popover.
- `--popover-padding`: The padding inside the Popover.
- `--popover-border-radius`: The border radius of the Popover.

Remember to set these variables in your project's root stylesheet, or provide them directly as inline styles in the `Popover` component. Failing to do so will result in the default browser styles being applied.

### Overriding CSS Variables
CSS variables can be overridden in your application by simply declaring them with new values in your CSS files. This is particularly useful if you want to apply custom themes or styles to the Popover component.

For example, if you want to change the default color, background color, and border color for Popovers across your app, you can add the following to your CSS:

```css
:root {
  --popover-color: #color1;
  --popover-background-color: #color2;
  --popover-border-color: #color3;
}
```
Then replace #color1 and #color2 with the color values you prefer. 