<template>
  <span>
    <a :disabled="disabled" :style="customStyle" v-if="out" :href="href"><slot></slot></a>
    <NuxtLink :disabled="disabled" :style="customStyle" v-else :to="href"><slot></slot></NuxtLink>
  </span>
</template>

<script>
export default {
  name: "WsLink",
  props: {
    out: { type: Boolean, default: false },
    href: { type: String, required: true },
    customStyle: { type: String, default: "" },
    disabled: { type: Boolean, required: false },
  },
};
</script>