# mac-ui

> Simple mac ui componets

# Demo

# Installation

```bash
$ npm install mac-ui --save

# or with yarn

$ yarn add mac-ui
```

# Usage

```html
<template>
  <div>
    <MacUi>Female</MacUi>
  <div>
</template>
<script>
  import MacUi from "mac-ui";
  export default {
    components: {
      MacUi
    }
  }
</script>
```

# Props

<table>
  <thead>
    <tr>
      <th>Prop</th>
      <th>Type</th>
      <th>Default</th>
      <th>Required</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Title</td>
      <td>String</td>
      <td>""</td>
      <td>No</td>
      <td>The next to the radio</td>
    </tr>
  </tbody>
</table>

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Run the linter

```
npm run lint
```

### Compiles and minifies for production

```
npm run build
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
