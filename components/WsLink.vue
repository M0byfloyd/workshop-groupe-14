<template>
  <a  v-if="out" :href="href">
    <slot>

    </slot>
  </a>
  <nuxt-link  v-else :to="href">
    <slot>

    </slot>
  </nuxt-link>
</template>

<script>
export default {
  name: "WsLink",
  props: {
    out: {type: Boolean, default: false},
    href: { type: String, required: true}
  }
}
</script>
