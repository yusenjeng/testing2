---
title: Documentation of Solid UI Shasta
type: docs
---

# Welcome to the UI Shasta

{{< columns >}}

## Installation

Install solid-ui-shasta with your preferred package manager. Use the following command with pnpm:

```sh
pnpm i solid-ui-shasta
```

Alternatively, **npm install** or **yarn add** will also work.

<--->

## Simplify and Shine

`solid-ui-shasta` is a sleek and powerful collection of UI components built with **SolidJS** and **TypeScript**. It enables developers to quickly create modern web applications with a minimalist design aesthetic.

{{< /columns >}}

## Get Started

To quickly set up and utilize solid-ui-shasta in your TypeScript project, follow these steps:

1. Include the necessary dependencies in your HTML file:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/iconoir-icons/iconoir@main/css/iconoir.css">
```

These dependencies include default font styles from Google Fonts and the Iconoir icon set, which is licensed under the MIT License.

2. Build and run your TypeScript project with the following code:
```ts
import { GlobalStyle, Text } from "solid-ui-shasta"

const App = () => {
  return <GlobalStyle>
    <Text>Hello</Text>
  </GlobalStyle>
}
```
Executing this code will render the "Hello" text with the default styles applied.

By following these steps, you can quickly integrate solid-ui-shasta into your solidjs project. 

Have Fun!

## Resources

Here are some helpful resources:

[GitHub](): Visit our repository to explore the code.

[Twitter](): Follow us on Twitter for news.

[Showcases](): Check out our showcases page to see more examples.
