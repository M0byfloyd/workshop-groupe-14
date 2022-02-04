<template>
  <label>
    <WsText>
      <slot>

      </slot>
    </WsText>
  </label>
</template>

<script>
import WsText from "~/components/WsText";
export default {
name: "WsLabel",
  components: {WsText}
}
</script>
