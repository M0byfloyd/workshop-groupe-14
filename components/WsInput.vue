<template>
  <div class="ws-input">
    <WsText :tag="label">
      {{ label }}
    </WsText>
    <input :type="type" />
  </div>
</template>

<script>
import WsText from "~/components/WsText";
export default {
  name: "WsInput",
  components: { WsText },
  props: {
    type: { type: String, default: "text" },
    label: { type: String, required: true },
  },
};
</script>

<style lang="scss" scoped>
.ws-input {
  display: flex;
  flex-direction: column;
}
</style>
