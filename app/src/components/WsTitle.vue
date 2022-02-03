<template>
  <component :is="tag">
    <slot>

    </slot>
  </component>
</template>

<script>
export default {
  name: "Title",
  props: {
    tag: { type: String, default: 'h1'}
  }
}
</script>