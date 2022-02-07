<template>
  <component :style="customStyle" :is="tag"><slot></slot></component>
</template>

<script>
export default {
  name: "WsText",
  props: {
    tag: { type: String, default: "span" },
    customStyle: { type: String, required: false },
  },
};
</script>
