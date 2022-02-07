<template>
  <div class="ws-input">
    <WsText class="input-label" tag="label">
      <slot></slot>
    </WsText>
    <input
      :value="value"
      @input="$emit('input', $event.target.value)"
      :placeholder="placeholder"
      :type="type"
      
    />
    <WsText
      v-if="warningMessage"
      class="warning-message"
      customStyle="color: var(--color-error)"
      tag="small"
      ><div>
        <svg
          width="12"
          height="12"
          viewBox="0 0 12 12"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M11.3334 6.00008C11.3334 8.94625 8.94539 11.3334 6.00008 11.3334C3.05477 11.3334 0.666748 8.94625 0.666748 6.00008C0.666748 3.05563 3.05477 0.666748 6.00008 0.666748C8.94539 0.666748 11.3334 3.05563 11.3334 6.00008ZM6.00008 7.07535C5.45374 7.07535 5.01083 7.51825 5.01083 8.0646C5.01083 8.61094 5.45374 9.05384 6.00008 9.05384C6.54642 9.05384 6.98933 8.61094 6.98933 8.0646C6.98933 7.51825 6.54642 7.07535 6.00008 7.07535ZM5.06088 3.51952L5.2204 6.44425C5.22787 6.58111 5.34103 6.68825 5.47808 6.68825H6.52208C6.65913 6.68825 6.7723 6.58111 6.77976 6.44425L6.93929 3.51952C6.94735 3.37169 6.82965 3.24739 6.68161 3.24739H5.31853C5.17049 3.24739 5.05281 3.37169 5.06088 3.51952V3.51952Z"
            fill="var(--color-error)"
          />
        </svg>
        {{ warningMessage }}
      </div>
    </WsText>
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
    value: { type: String, default: "" },
    warningMessage: { type: String, required: false },
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

.warning-message {
  font-weight: var(--font_weight-semibold);
}

.warning-message::before {
  content: url("/error.svg");
  background-image: url("/error.svg");
}
</style>
