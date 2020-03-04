<template>
  <div id="app">
    <p>Current Gender: {{ currentGender }}</p>
    <GenderChooser v-model="currentGender" />

    <fieldset>
      <legend>Editor</legend>
      <Checkbox name="editor" value="code">DO</Checkbox>

      <Checkbox name="editor" value="vim">VIM</Checkbox>
    </fieldset>
    <input type="checkbox" />
  </div>
</template>

<script>
import { Radio, Checkbox } from "./components/UI";
import GenderChooser from "./components/GenderChooser";
export default {
  name: "App",
  components: {
    Radio,
    Checkbox,
    GenderChooser
  },
  data() {
    return {
      currentGender: "Female"
    };
  }
};
</script>
