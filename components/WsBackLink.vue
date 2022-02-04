<template>
  <div class="back-link-container">
    <div class="arrow" v-if="hasIcon"></div>
    <NuxtLink class="back-link" :to="link">{{ linkText }}</NuxtLink>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    link: String,
    linkText: String,
    hasArrow: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.back-link-container {
  cursor: pointer;
}

.arrow {
  background: #000;
  height: 2px;
  width: 25px;
  position: relative;

  &::before,
  &::after {
    content: "";
    background: #000;
    position: absolute;
    height: 2px;
    border-radius: 5px;
    width: 10px;
  }

  &::before {
    left: -2px;
    bottom: -3px;
    transform: rotate(45deg);
  }

  &::after {
    left: -2px;
    top: -3px;
    transform: rotate(-45deg);
  }
}
</style>
