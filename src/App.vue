<template>
  <div id="app">
    <p>Gender: {{ currentGender }}</p>
    <GenderChooser v-model="currentGender" />
  </div>
</template>

<script>
// import Radio from "./components/Radio";
// import Checkbox from "./components/Checkbox";
import GenderChooser from "./components/GenderChooser";

export default {
  name: "App",
  components: {
    GenderChooser
  },
  data() {
    return {
      currentGender: "Female"
    };
  }
};
</script>
