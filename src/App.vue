<template>
  <div id="app">
    <fieldset>
      <legend>Gender Chooser</legend>
      <Radio name="gender" value="Female">Female</Radio>
      <Radio name="gender" value="Male">Male</Radio>
    </fieldset>

    <fieldset>
      <legend>Editor</legend>
      <Checkbox name="editor" value="code">VS Code</Checkbox>
      <Checkbox name="editor" value="sublime">Sublime Text</Checkbox>
      <Checkbox name="editor" value="vim">VIM</Checkbox>
    </fieldset>
  </div>
</template>

<script>
import Radio from "./components/Radio";
import Checkbox from "./components/Checkbox";

export default {
  name: "App",
  components: {
    Radio,
    Checkbox
  }
};
</script>
