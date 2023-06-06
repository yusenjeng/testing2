# `<Dropdown />`

Dropdown component is a customizable dropdown menu component. It provides control over several aspects of styling, such as color, padding, border, etc., along with behavior, like selected item and disabled state. It can be easily adapted to suit a variety of styles and use-cases.

## Quick Sample Code
```jsx
import { Dropdown, DropdownOption } from 'solid-ui-shasta'

function App() {
  return (
    <Dropdown defaultLabel="Select an option" onChange={val => console.log(val)}>
      <DropdownOption label="Option 1" value="1" />
      <DropdownOption label="Option 2" value="2" />
    </Dropdown>
  )
}
```

## Props

Here is a list of all the props that the `Dropdown` component accepts:

| Prop | Type | Description |
| --- | --- | --- |
| `children` | JSX.Element or JSX.Element[] | The `DropdownOption` components to be rendered inside the dropdown. |
| `defaultLabel` | string | The default label to be shown when no option is selected. |
| `onChange` | function | Handler to be invoked when an option is selected. |
| `disabled` | boolean | If `true`, the dropdown will be disabled. |
| `class` | string | The CSS class of the dropdown. |
| `style` | string | The CSS style of the dropdown. |

## More Samples

Here's an example of how to use the Dropdown component:

### Disabled Dropdown
```jsx
<Dropdown defaultLabel="Select an option" disabled>
  <DropdownOption label="Option 1" value="1" />
  <DropdownOption label="Option 2" value="2" />
</Dropdown>
```

### Styled Dropdown
This code demonstrates a custom-styled `<Dropdown />` component. The **customClass** and **customStyle** constants provide a CSS class name and inline styles respectively. These styles define the border, background color, font size, text color, and hover effect of the dropdown.

The dropdown shows "Select an option" as the default label and has two options. When an option is selected, its value is logged to the console. The **class** and **style** props apply the custom styles to the dropdown, and the `<DropdownOption />` components define the options available for selection.
```jsx
const customClass = 'dummy-class-name'
const customStyle = `
border: 4px solid #E83F6F;  
background-color: #E83F6F;
font-size: 1.5rem;
color: #fff;
&:hover{
  box-shadow: 0 0 4px #E83F6F;
}
`

<Dropdown
  defaultLabel="Select an option"
  class={customClass}
  style={customStyle}
  onChange={val => console.log(val)}
>
  <DropdownOption label="Option 1" value="1" />
  <DropdownOption label="Option 2" value="2" />
</Dropdown>
```

## CSS

The `<Dropdown />` component uses CSS variables for styling. Here's a brief description of each variable:

- `--color-primary`: The color of the dropdown text and border.
- `--background-color`: The background color of the dropdown.

These variables are used in the component's base styling. To override these, provide the `style` prop with your custom styles or assign a class name to the `class` prop and define the styles in your CSS file.

### Overriding CSS Variables
To alter the CSS variables in your application, you just need to define them with new values in your CSS files.
```css
:root {
  --color-primary: #color1;
  --background-color: #color2;
}
```
In addition, by supplying custom **ThemeProps** to the `<GlobalStyle />` component, you can override the CSS variables directly.