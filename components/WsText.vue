<template>
  <component :is="tag">
    <slot>

    </slot>
  </component>
</template>

<script>
export default {
name: "WsText",
  props : {
  tag :{ type: String, default: 'span' }
  }
}
</script>
