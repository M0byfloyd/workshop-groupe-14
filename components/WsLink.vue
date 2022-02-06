<template>
  <span>
    <a :style="customStyle" v-if="out" :href="href"
      ><slot></slot
    ></a>
    <NuxtLink :style="customStyle" v-else :to="href"
      ><slot></slot
    ></NuxtLink>
  </span>
</template>

<script>
export default {
  name: "WsLink",
  props: {
    out: { type: Boolean, default: false },
    href: { type: String, required: true },
    customStyle: {
      default: "",
      type: String,
    },
  },
};
</script>
