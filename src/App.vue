<template>
  <div id="app">
    <fieldset>
      Gender: {{ gender }}
      <legend>Radio</legend>
      <Radio @input="handleChange" name="gender" :checked="true" value="male">
        Male
      </Radio>
      <Radio @input="handleChange" name="gender" value="female">
        Female
      </Radio>
    </fieldset>

    <fieldset>
      <legend>Editor</legend>
      <p>Editors: {{ editors.join(", ") }}</p>
      <Checkbox @input="handleCheckbox" name="editor" value="code">
        Code
      </Checkbox>

      <Checkbox @input="handleCheckbox" name="editor" value="vim">
        VIM
      </Checkbox>
    </fieldset>
    <input type="checkbox" />
  </div>
</template>

<script>
// import Radio from "./components/Radio.vue";
// import Checkbox from "./components/Checkbox.vue";
import { Radio, Checkbox } from "./components/UI";
export default {
  name: "App",
  components: {
    Radio,
    Checkbox
  }
};
</script>
