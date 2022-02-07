<template>
  <div
    :style="`width: ${width}; height: ${height}`"
    :class="`ws-img ${alignProperties[align]}`"
  >
    <img src="/mail.png" class="" :alt="alt" />
  </div>
</template>

<script>
export default {
  name: "WsButton",
  props: {
    alt: { type: String, required: false },
    src: { type: String, required: true },
    width: { type: String, required: true },
    height: { type: String, required: true },
    align: { type: String, default: "center" },
  },
  data() {
    return {
      alignProperties: {
        center: "align-center",
        left: "align-left",
        right: "align-right",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.ws-img img {
  height: 100%;
  width: 100%;
  object-fit: contain;
}

.align-center {
  margin: auto;
}

.align-right {
  margin-left: auto;
}

.align-left {
  margin-right: auto;
}
</style>
