<template>
  <div class="ws-input">
    <WsText class="input-label" tag="label">
      <slot></slot>
    </WsText>
    <input :placeholder="placeholder" :type="type" />
  </div>
</template>

<script>
import WsText from "~/components/WsText";

export default {
  name: "WsInput",
  components: { WsText },
  props: {
    type: { type: String, default: "text" },
    placeholder: { type: String, default: "" },
  },
};
</script>

<style lang="scss" scoped>
.input-label {
  margin-bottom: var(--space-s);
}

.ws-input {
  display: flex;
  flex-direction: column;
}
</style>
