<template>
  <div class="back-link-container">
    <div class="arrow" v-if="hasArrow"></div>
    <WsLink
      class="back-link"
      :customStyle="{ color: 'var(--color-black)' }"
      :href="link"
    >
      {{ linkText }}
    </WsLink>
  </div>
</template>

<script>
import WsLink from "~/components/WsLink";

export default {
  name: "",
  props: {
    link: { type: String, default: "/" },
    linkText: { type: String, default: "Back" },
    hasArrow: { type: Boolean, default: true },
  },
  components: {
    WsLink,
  },
};
</script>

<style lang="scss" scoped>
.back-link-container {
  cursor: pointer;
  display: flex;
  align-items: flex-end;
}

.back-link {
  color: var(--color-black);
}

.arrow {
  background: var(--color-black);
  height: 1px;
  width: 15px;
  position: relative;
  transform: translateY(-8.5px);
  margin-right: 1px;

  &::before,
  &::after {
    content: "";
    background: var(--color-black);
    position: absolute;
    height: 1px;
    border-radius: 5px;
    width: 6px;
    left: -1px;
  }

  &::before {
    bottom: -2px;
    transform: rotate(50deg);
  }

  &::after {
    top: -2px;
    transform: rotate(-50deg);
  }
}
</style>
