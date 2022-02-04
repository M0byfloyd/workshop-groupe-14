<template>
  <WsBackLink link="/" linkText="Back" :hasArrow="false" />
</template>

<script>
import WsBackLink from "/components/WsBackLink";

export default {
  name: "reset-password",
  components: {
    WsBackLink,
  },
};
</script>
