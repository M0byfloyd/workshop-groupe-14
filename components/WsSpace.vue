<template>
  <div>
    <div
      v-if="horizontal"
      :style="`height: calc(var(--space-${size}) * ${scale});`"
    ></div>
    <div
      v-if="vertical"
      :style="`width: calc(var(--space-${size}) * ${scale});`"
    ></div>
  </div>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
      default: "m",
    },
    scale: {
      type: Number,
      default: 0,
    },
    horizontal: {
      type: Boolean,
      default: false,
    },
    vertical: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
