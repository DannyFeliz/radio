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

<style scoped>
fieldset {
  border-radius: 6px;
}
</style>
