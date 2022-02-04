<template>
  <span>
    <a :style="'color:' + customStyle.color" v-if="out" :href="href"><slot></slot></a>
    <NuxtLink :style="'color:' + customStyle.color" v-else :to="href"><slot></slot></NuxtLink>
  </span>
</template>

<script>
export default {
  name: "WsLink",
  props: {
    out: { type: Boolean, default: false },
    href: { type: String, required: true },
    customStyle: {
      color: "var(--color-primary)",
    },
  },
};
</script>
