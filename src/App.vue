<template>
  <div id="app">
    <Radio />
    <Checkbox />
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
