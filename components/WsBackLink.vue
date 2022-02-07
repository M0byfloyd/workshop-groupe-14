<template>
  <WsLink
    class="back-link"
    :customStyle="'color: var(--color-black)'"
    :href="link"
  >
    <div class="back-link-container">
      <div class="arrow" v-if="hasArrow"></div>

      {{ linkText }}
    </div>
  </WsLink>
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
  display: inline-flex;
  align-items: flex-end;
  width: min-content;
}

.back-link {
  color: var(--color-gray_dark);
  cursor: pointer;
}

.arrow {
  background: var(--color-gray_dark);
  height: 1px;
  width: 15px;
  position: relative;
  transform: translateY(-8.5px);
  margin-right: 1px;

  &::before,
  &::after {
    content: "";
    background: var(--color-gray_dark);
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
