<template>
  <WsText :is="tag">
    <slot>
      
    </slot>
  </WsText>
</template>
<script>
import WsText from "~/components/WsText";

export default {
  name: "WsTitle",
  components: {WsText},
  props: {
    tag: {type: String, default: 'h1'}
  }
}
</script>
