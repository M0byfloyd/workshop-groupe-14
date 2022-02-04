<template>
  <button :type="type" :class="[]">
    <slot> </slot>
  </button>
</template>

<script>
export default {
  name: "WsButton",
  props: {
    type: { type: String, required: false },
    color: { type: String, default: "primary" },
    backgroundColor: { type: String, default: "primary" },
    borderColor: { type: String, default: "primary" },
    borderWidth: { type: String, default: "primary" },
    borderRadius: { type: String, default: "primary" },
  },
};
</script>
