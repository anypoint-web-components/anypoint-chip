[![Published on NPM](https://img.shields.io/npm/v/@anypoint-web-components/anypoint-chip.svg)](https://www.npmjs.com/package/@anypoint-web-components/anypoint-chip)

[![Build Status](https://travis-ci.org/anypoint-web-components/anypoint-chip.svg?branch=stage)](https://travis-ci.org/anypoint-web-components/anypoint-chip)

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/anypoint-web-components/anypoint-chip)

# anypoint-chip

A compact material design element that represent and input, attribute, or action.

### Example

```html
<style>
.avatar {
  background-color: red;
  color: #fff !important;
  width: 24px;
  height: 24px;
}
</style>
<h2>Basics</h2>
<section>
  <anypoint-chip>Simple chip</anypoint-chip>

  <anypoint-chip>
    <span class="avatar" slot="icon">C</span>
    <span>Chip with icon</span>
  </anypoint-chip>

  <anypoint-chip removable>
    <span class="avatar" slot="icon">R</span>
    Chip that can be removed
  </anypoint-chip>

  <anypoint-chip removable disabled>
    <span class="avatar" slot="icon">D</span>
    Disabled chip
  </anypoint-chip>
</section>

<h2>Input chips</h2>
<section>
  <anypoint-chip removable>
    <iron-icon icon="communication:location-on" slot="icon"></iron-icon>
    Portland
  </anypoint-chip>

  <anypoint-chip removable>
    <iron-icon icon="maps:directions-bike" slot="icon"></iron-icon>
    Biking
  </anypoint-chip>
</section>
```

### API components

This components is a part of [API components ecosystem](https://elements.advancedrestclient.com/)

## Usage

### Installation
```
npm install --save @anypoint-web-components/anypoint-chip
```

### In an html file

```html
<html>
  <head>
    <script type="module">
      import './node_modules/@anypoint-web-components/anypoint-chip/anypoint-chip.js';
    </script>
  </head>
  <body>
    <anypoint-chip></anypoint-chip>
  </body>
</html>
```

### In a LitElement

```js
import { LitElement, html } from 'lit-element';
import '@anypoint-web-components/anypoint-chip/anypoint-chip.js';

class SampleElement extends PolymerElement {
  render() {
    return html`
    <anypoint-chip></anypoint-chip>
    `;
  }
}
customElements.define('sample-element', SampleElement);
```

## Development

```sh
git clone https://github.com/anypoint-web-components/anypoint-chip
cd anypoint-chippolymer test --npm
npm install
```

### Running the demo locally

```sh
npm start
```

### Running the tests

```sh
npm test
```

## Styling

`<anypoint-chip>` provides the following custom properties for styling:

Custom property | Description | Default
----------------|-------------|----------
`--anypoint-chip-background-color` | Chip background color | `rgba(35, 47, 52, 0.12)`
`--anypoint-chip-focused-background-color` | Background color when focused | `#D6D6D6`
`--anypoint-chip-active-background-color` | Background color when toggle is active | `#cdcdcd`
`--anypoint-chip-icon-color` | Color of the icon | `#666666`
`--anypoint-chip-label-color` | Color of the label | `#232F34`
`--anypoint-chip-label-focused-color` | Color of the when focused | ``
`--anypoint-chip-label-active-color` | Color of the when active | ``
`--anypoint-chip-icon-close-color` | Color of the close icon | `#dfdfdf`
`--anypoint-chip-icon-close-background-color` | Background color of the close icon | `#666666`

`<anypoint-chip>` provides the following [parts](https://www.w3.org/TR/css-shadow-parts-1/):

Part name | Description
----------------|-------------
`anypoint-chip-container` | Styles applied to the chip container
`anypoint-chip-icon` | Styles applied to the icon container
`anypoint-chip-label` | Styles applied to the label container
`anypoint-chip-remove` | Styles applied to the delete icon
