<template>
  <span class="ui-acme-container">
    <label :for="`checkbox-${id}`">
      <input
        v-bind="$attrs"
        v-on="$listeners"
        type="checkbox"
        :id="`checkbox-${id}`"
      />
      <span class="checkbox">
        <svg width="12px" height="11px" viewBox="0 0 12 11">
          <polyline points="1 6.29411765 4.5 10 11 1" />
        </svg>
      </span>
      <span>
        <slot />
      </span>
    </label>
  </span>
</template>

<script>
export default {
  name: "Checkbox",
  data() {
    return {
      id: Math.random()
        .toString(16)
        .substring(2)
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
    &[type="checkbox"] {
      position: absolute;
      opacity: 0;
    }

    &[type="checkbox"]:checked + .checkbox {
      background-color: #606062;
      background-image: linear-gradient(#255cd2, #1d52c1);

      svg {
        stroke-dashoffset: 0;
        transition: all 0.15s ease;
      }
    }
  }

  .checkbox + span {
    float: left;
    margin-left: 6px;
  }

  .checkbox {
    position: relative;
    display: block;
    float: left;
    width: 18px;
    height: 18px;
    border-radius: 4px;
    background-color: #606062;
    background-image: linear-gradient(#474749, #606062);
    box-shadow: inset 0 1px 1px rgba(255, 255, 255, 0.15),
      inset 0 -1px 1px rgba(0, 0, 0, 0.15);
    transition: all 0.15s ease;

    svg {
      position: absolute;
      top: 3px;
      left: 3px;
      fill: none;
      stroke-linecap: round;
      stroke-linejoin: round;
      stroke: #fff;
      stroke-width: 2;
      stroke-dasharray: 17;
      stroke-dashoffset: 17;
      transform: translate3d(0, 0, 0);
    }
  }
}
</style>
