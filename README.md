<p align="center"><img src="https://cogoport.github.io/cogo-toast/static/meta/android-chrome-96x96.png" alt="cogo-toast" title="cogo-toast" width="120"><p>
<h1 align="center">Cogo Toast</h1>
<p align="center" style="font-size: 1.2rem;">Beautiful, Zero Configuration, Toast Messages for React</p>
<p align="center"><a href="https://cogoport.github.io/cogo-toast/">https://cogoport.github.io/cogo-toast/</a></p>

[![Dependencies](https://img.shields.io/david/Cogoport/cogo-toast.svg)](https://david-dm.org/Cogoport/cogo-toast.svg)
[![DevDependencies](https://img.shields.io/david/dev/Cogoport/cogo-toast.svg)](https://david-dm.org/Cogoport/cogo-toast?type=dev)
[![npm package](https://img.shields.io/npm/v/cogo-toast/latest.svg)](https://www.npmjs.com/package/cogo-toast)
[![Small size](https://img.badgesize.io/https://unpkg.com/cogo-toast/dist/index.js?compression=gzip)](https://unpkg.com/cogo-toast/dist/index.js)
[![npm downloads](https://img.shields.io/npm/dm/cogo-toast.svg)](https://www.npmjs.com/package/cogo-toast)
![Code style](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)
[![License](https://img.shields.io/npm/l/@xstyled/styled-components.svg)](https://github.com/Cogoport/cogo-toast/blob/master/LICENSE)

<p align="center"><img src="docs/static/images/preview.png" alt="cogo-toast-preview" title="cogo-toast-preview"><p>

### Install via NPM:

```bash
npm install --save cogo-toast
```

### Install via Yarn:

```bash
yarn add cogo-toast
```

#### Note:

The latest version `^3.0.0` makes the use of React Hooks internally.

To use this package in projects that don't support hooks, use `v2.0.1` instead.

```bash
yarn add cogo-toast@2.0.1
```

## Usage

Its Plug and Play. No configuration required. Just import and you are good to go.

```javascript
import cogoToast from 'cogo-toast';

cogoToast.success('This is a success message!');
```

### 5 Built in Types

There are 5 built-in types to handle the most common cases in any application.

```javascript
cogoToast.success('This is a success message');

cogoToast.info('This is a info message');

cogoToast.loading('This is a loading message');

cogoToast.warn('This is a warn message');

cogoToast.error('This is a error message');
```

### Use JSX

**cogoToast** is built using React. Which means any valid jsx can be used as the message in cogoToast

```javascript
cogoToast.info(
  <div>
    <b>Awesome!</b>
    <div>Isn't it?</div>
  </div>,
);
```

### Returns a Promise

Returns a promise which resolves when the toast is about to hide.

This can be useful to do some action when the toast has completed showing.

```javascript
cogoToast.loading('Loading your data...').then(() => {
	cogoToast.success('Data Successfully Loaded');
});
```

When hideAfter = 0, It returns a callback function that hides the toast, instead of a promise.

### Hide on Click

```javascript
cogoToast.success('This is a success message.', {
	onClick: hide => {
		hide();
	},
});
```

### Completely Customizable

The second parameter to the function is an options object that can be passed in for customization.

```javascript
cogoToast.info('This is an info message', options);
```

#### All Available Options

Here's a list of all the available options, to customize the toast to your needs.

|    Options    |                                               Type                                               |                          Default                           |
| :-----------: | :----------------------------------------------------------------------------------------------: | :--------------------------------------------------------: |
|   hideAfter   |                                        Number in Seconds                                         | `3` <br />(Can be `0` to disable auto-hiding of the toast) |
|   position    | `'top-left', 'top-center', 'top-right',` <br /> `'bottom-left', 'bottom-center', 'bottom-right'` |                       `'top-center'`                       |
|    heading    |                                              String                                              |                            `''`                            |
|  renderIcon   |                                       Function<ReactNode>                                        |                   Icon Based on the Type                   |
|      bar      |           Object <br /> `{ size: '2px', style: 'solid/dashed/dotted', color: '#hex' }`           |                     Based on the Type                      |
| onClick(hide) |                                             Function                                             |                           `null`                           |

#### Custom Styling

You can provide your own custom styling by extending the `ct-toast` class in your css styles.

For all classnames, refer to [/src/styles/styles.css](/src/styles/styles.css)

### Only ~ 4K Gzipped

The package contains the minified build file, along with the SVG Icons and the Styles, built into the Code, with a total of ~4K Gzipped

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/anmolmahatpurkar"><img src="https://avatars2.githubusercontent.com/u/36692003?v=4" width="100px;" alt="Anmol Mahatpurkar"/><br /><sub><b>Anmol Mahatpurkar</b></sub></a><br /><a href="https://github.com/Cogoport/cogo-toast/commits?author=anmolmahatpurkar" title="Code">💻</a> <a href="#design-anmolmahatpurkar" title="Design">🎨</a> <a href="https://github.com/Cogoport/cogo-toast/commits?author=anmolmahatpurkar" title="Documentation">📖</a></td>
  </tr>
</table>

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
