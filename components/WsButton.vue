<template>
  <button :type="type" :class="[]">
    <slot> </slot>
  </button>
</template>

<script>
export default {
  name: "WsButton",
  props: {
    type: { type: String, default: "button" },
  },
};
</script>
