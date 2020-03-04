### Checkbox / Radio

- v-bind="\$attrs"
- v-on="\$listener"
- slot
- unique id
  - Math.random()
    .toString(16)
    .substring(2)

### Tree Shaking

```js
// App.js
import { Radio, Checkbox } from "./components/UI";
```

---

```html
// UI.js import Checkbox from "./Checkbox.vue"; import Radio from "./Radio.vue";
export { Checkbox, Radio };
```

### GenderChooser

```vue
<template>
  <fieldset>
    <legend>Gender</legend>
    <Radio
      @input="handleGender"
      name="gender"
      value="Male"
      :checked="$attrs.value == 'Male'"
      >Male</Radio
    >

    <Radio
      @input="handleGender"
      name="gender"
      value="Female"
      :checked="$attrs.value == 'Female'"
      >Female</Radio
    >
  </fieldset>
</template>

<script>
import Radio from "./Radio";
export default {
  name: "GenderChooser",
  components: {
    Radio
  },
  methods: {
    handleGender({ target: { value } }) {
      this.$emit("input", value);
    }
  }
};
</script>
```

### Example

# Optimization

```js
// vue.config.js
module.exports = {
  css: {
    extract: false
  }
};
```

```json
// package.json
"sideEffects": [
  "*.vue"
],
```

### After build

Show the compiled js and css
