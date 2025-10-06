<div align="center">
  <a href="https://www.react-pdf.dev/?utm_source=github&utm_medium=referral" target="_blank">
    <picture>
      <source srcset="./assets/img/react-pdf_cover.webp" width="100%">
      <img alt="React PDF" src="./assets/img/react-pdf_cover.webp width="100%">
    </picture>
  </a>
</div>

<br/>
<div align="center">
  Works seamlessly on your React or Next.js websites. Fast, Customizable and Web Responsive PDF viewer. Save you weeks of development time.
</div>  
<br/>

<div align="center">
  
  [React PDF Home][reactpdf] - [License](#page_facing_up-license) - [Documentation][reactpdf-docs]

[![NPM Version](https://img.shields.io/npm/v/%40pdf-viewer%2Freact)][npm]
[![Twitter](https://img.shields.io/twitter/follow/ReactPDF?label=ReactPDF&style=social)][twitter]

</div>

# :star: Why React PDF

- **Save Weeks of Development Time**: React PDF simplifies PDF integration with ready-to-use tools, minimizing the need for custom development and saving you valuable time.
- **Tailored for React.js**: React PDF is native to React.js, ensuring smooth integration into your projects.
- **Customizability at Its Core**: Built with flexibility in mind, allowing you to match your application’s unique style and functionality.
- **High-Performance & Rapid Rendering**: Optimized for rendering large PDFs efficiently, React PDF delivers lightning-fast load times with features like virtual scrolling.
- **Accessibility**: Designed with inclusivity in mind, React PDF supports ARIA attributes, catering to diverse user bases.
- **Modern Browser Compatibility**: Works seamlessly across modern browsers, eliminating compatibility headaches.
- **Active Development & Support**: With regular updates and a responsive support team, React PDF evolves to meet developer needs.

# 📜 Background

As developers ourselves, we faced many issues such as browser incompatibility and customizability while trying to render a PDF document or working with PDF libraries. Having faced issues using PDF libraries, we want the solution to be flexible for React.js developers and teams. More importantly, the technical document must be easy to use!

# :sparkles: Features

- 🎯 **Interactive & Immersive Viewing Experience** with features like rotation, zoom, and keyboard navigation.
- 📱 **Responsive Across All Devices** for a consistent experience on desktops, tablets and mobile devices.
- 🎨 **Customizable UI and Styling** to tailor the viewer’s appearance to match your website’s theme.
- 🧭 **Advanced Navigation Options** to browse documents easily with table of contents, hyperlinks, and a powerful search tool.
- ⚡ **High-Performance Rendering** to load large PDF documents quickly and handle complex elements like vector graphics with ease.
- 🔧 **Programmatic Control with Hooks and Props**, allowing you to interact with the viewer programmatically.
- 📂 **Document Management Tools**, including features like downloading and printing.
- 👁️ **Accessibility Support** to built-in support for ARIA attributes and tooltips, catering to diverse user bases.

For the full feature set, visit [React PDF Features](https://www.react-pdf.dev/features?utm_source=github&utm_medium=referral).

# :zap: Quick Start Guide

Here’s how to get started with React PDF in your React.js project:

## 1. Check Prerequsities

Here are the basic system requirements to run the React PDF component:

- React version: >= 18.0
- React version: >= 19.0

If you are working with a React framework such as Next and Gatsby, React PDF can run smoothly as long as you are using React 18 and above.

React PDF viewer also works well with other React.js UI libraries such as MUI, Ant Design and Chakra UI.

Although React PDF can run on most JavaScript module bundlers, it is more vigorously tested on Vite and Webpack.

_Remark: <br/>- If using TypeScript, it requires >= TypeScript 4.6._

### Browser support

| Chrome | Firefox | Edge | Safari | Safari iOS | Chrome Android |
| ------ | ------- | ---- | ------ | ---------- | -------------- |
| 115+   | 115+    | 115+ | 16.5+  | 16.5+      | 126+           |

## 2. Install the Package

There are a few ways you can install React PDF, namely `bun`, `npm`, `pnpm` or `yarn`.

### Using bun:

```bash
bun add @pdf-viewer/react
```

##### Caching of previous Worker version with `bun`

To clear cache, try running `bun pm cache rm` to remove cache in the global cache directory. If the error remains, try executing the following steps:

```shell
rm bun.lockb
rm -R node_modules
```

### Using npm:

```bash
npm install @pdf-viewer/react
```

### Using yarn:

```bash
yarn add @pdf-viewer/react
```

### Using pnpm:

```bash
pnpm add @pdf-viewer/react
```

For more information on how to use different package managers, please visit our [installation guide](https://docs.react-pdf.dev/introduction/getting-started/#installation?utm_source=github&utm_medium=referral).

## 3. Import and Use the Component

The following structure demonstrates how to build a React PDF viewer by importing and assembling components. This modular approach gives you the flexibility to customize the viewer as needed.

```tsx
  <RPConfig>               {/* Configuration license and pdfjs-dist worker */}
    <RPProvider>           {/* Viewer context provider */}
      <RPTheme>            {/* Theme customization (optional) */}
        <RPDefaultLayout>  {/* Default layout container */}
          <RPPages />      {/* PDF pages renderer */}
        </RPDefaultLayout>
      </RPTheme>
    </RPProvider>
  </RPConfig>
```

_Remark: For more information on each component, please refer to [Component](https://docs.react-pdf.dev/components/overview?utm_source=github&utm_medium=referral)._

### Basic Usage

The most basic usage of React PDF viewer needs four components, namely: `RPConfig`, `RPProvider`, `RPDefaultLayout`, and `RPPages`.

Here's how to implement a basic PDF viewer in a React application:

```jsx
import { RPProvider, RPDefaultLayout, RPPages, RPConfig } from '@pdf-viewer/react'

const App = () => {
  return (
    <RPConfig>
      <RPProvider src="https://cdn.codewithmosh.com/image/upload/v1721763853/guides/web-roadmap.pdf">
        <RPDefaultLayout style={{ height: '660px' }}>
          <RPPages />
        </RPDefaultLayout>
      </RPProvider>
    </RPConfig>
  )
}
export default App
```

The PDF viewer will automatically adjust to fit its container's dimensions. You can control the size by setting the `style` prop on `RPDefaultLayout`. For more information on using React PDF, visit our [basic usage guide](https://docs.react-pdf.dev/introduction/basic-usage?utm_source=github&utm_medium=referral)

You may also check out our [Starter Toolkit](#pushpin-starter-toolkit) for examples to get you started.

### 4. Customize with Hooks and Props

To enhance React PDF further, we offer built-in hooks and props that let you fine-tune functionality, adjust appearance, and integrate custom behaviors into your application.

For detailed usage, refer to our [Documentation][reactpdf-docs].

# :pushpin: Starter Toolkit

Here are some sample projects to get started on React PDF quickly:

1. [React (webpack) - JavaScript](https://github.com/pdf-viewer-react/starter-rp-react-js-webpack)
2. [React (webpack) - TypeScript](https://github.com/reactpdf/pdf-viewer-react/starter-rp-react-ts-webpack)
3. [React (vite) - JavaScript](https://github.com/pdf-viewer-react/starter-rp-react-js-vite)
4. [React (vite) - TypeScript](https://github.com/pdf-viewer-react/starter-rp-react-ts-vite)
6. [Next - JavaScript](https://github.com/pdf-viewer-react/starter-rp-next-js)
7. [Next - TypeScript](https://github.com/pdf-viewer-react/starter-rp-next-ts)
8. [Next - TypeScript - Turborepo](https://github.com/pdf-viewer-react/starter-rp-next-ts-turborepo)
9. [Remix - JavaScript](https://github.com/pdf-viewer-react/starter-rp-remix-js)
10. [Remix - TypeScript](https://github.com/pdf-viewer-react/starter-rp-remix-ts)


# 📝 Changelog

Check out our latest release [v1.9.1 (3 October 2025)](https://docs.react-pdf.dev/introduction/changelog/#v191-3-october-2025?utm_source=github&utm_medium=referral)


# :raising_hand: Need Help?

We are more than happy to help you. If you have any questions, run into any errors or face any problems, please feel free to create an issue in [Issues](../../issues) or PM us directly in [Twitter][twitter]. Anything related to React PDF is on the table!

# :page_facing_up: License

React PDF is distributed under our proprietary license. Please refer to our [License page](https://www.react-pdf.dev/license-agreement?utm_source=github&utm_medium=referral) file for more details.

If you would like to use React PDF commercially, please purchase a license from [our website][reactpdf] or reach out to us directly at [david@react-pdf.dev](mailto:david@react-pdf.dev).


# Acknowledgement

- [pdf.js](https://github.com/mozilla/pdf.js)
- [Img Shields](https://shields.io)
- [React.js](https://reactjs.org/)

[reactpdf]: https://www.react-pdf.dev/?utm_source=github&utm_medium=referral
[reactpdf-docs]: https://docs.react-pdf.dev/?utm_source=github&utm_medium=referral
[npm]: https://www.npmjs.com/package/@pdf-viewer/react
[twitter]: https://www.x.com/ReactPDF
