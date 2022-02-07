<template>
  <div>
    <WsText tag="h1">Sign up</WsText>
    <WsSpace size="s" :horizontal="true" />
    <WsText tag="p"
      >Already got an account? <WsLink href="/">Sign in</WsLink></WsText
    >
    <WsSpace size="l" :scale="1.5" :horizontal="true" />
    <WsInput v-model="email" type="email" placeholder="joe.lee@gmail.com"
      >Email</WsInput
    >
    <WsSpace size="m" :horizontal="true" />
    <WsInput v-model="password" type="password" placeholder="**********"
    warningMessage="Message d'erreur "
      >Password</WsInput
    >
    <WsSpace size="l" :horizontal="true" />
    <WsButton :disabled="!checkInputs">Sign up</WsButton>
  </div>
</template>

<script>
import WsText from "~/components/WsText";
import WsLink from "~/components/WsLink";
import WsInput from "~/components/WsInput";
import WsButton from "~/components/WsButton";

export default {
  name: "signup",
  components: { WsButton, WsInput, WsLink, WsText },
  computed: {
    checkInputs() {
      return this.email && this.password ? true : false;
    },
  },
  data() {
    return {
      email: "",
      password: "",
    };
  },
};
</script>
