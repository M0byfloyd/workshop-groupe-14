<template>
  <button :disabled="disabled" :type="type">
    <slot> </slot>
  </button>
</template>

<script>
export default {
  name: "WsButton",
  props: {
    type: { type: String, default: "button" },
    disabled: { type: Boolean, default: false },
  },
};
</script>
