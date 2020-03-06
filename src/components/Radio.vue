<template>
  <span class="ui-acme-container">
    <label :for="`radio-input`">
      <input
        v-bind="$attrs"
        v-on="$listeners"
        type="radio"
        :id="`radio-${id}`"
      />
      <span class="radio"></span>
      <span>
        <slot />
      </span>
    </label>
  </span>
</template>

<script>
const abc = "hello"
export default {
  name: "Radio",
  data() {
    return {
      id: Math.random()
        .toString(16)
        .substr(2)
    };
  }
};
</script>

<style lang="scss">
.ui-acme-container {
  font-family: -apple-system, BlinkMacSystemFont, "myriad-pro", sans-serif;
  font-weight: 400;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: inline-block;

  label {
    margin: 10px;
    cursor: pointer;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  input {
    &[type="radio"] {
      position: absolute;
      opacity: 0;

      &:checked + .radio {
        background-color: #606062;
        background-image: linear-gradient(#255cd2, #1d52c1);

        &:after {
          opacity: 1;
          transform: scale(1);
          transition: all 0.15s ease;
        }
      }
    }
  }

  .radio + span {
    float: left;
    margin-left: 6px;
  }

  .radio {
    position: relative;
    display: block;
    float: left;
    width: 18px;
    height: 18px;
    border-radius: 10px;
    background-color: #606062;
    background-image: linear-gradient(#474749, #606062);
    box-shadow: inset 0 1px 1px rgba(255, 255, 255, 0.15),
      inset 0 -1px 1px rgba(0, 0, 0, 0.15);
    transition: all 0.15s ease;

    &:after {
      content: "";
      position: absolute;
      display: block;
      top: 6px;
      left: 6px;
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: #fff;
      opacity: 0;
      transform: scale(0);
    }
  }
}
</style>
