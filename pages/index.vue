<template>
  <div>
    <WsText tag="h1"> Sign in </WsText>
    <WsSpace size="s" :horizontal="true" />
    <WsText tag="p"
      >Not signed-up? <WsLink href="/signup">Register</WsLink></WsText
    >
    <WsSpace size="l" :scale="1.5" :horizontal="true" />
    <WsInput v-model="email" type="email" placeholder="joe.lee@gmail.com"
      >Email</WsInput
    >
    <WsSpace size="m" :horizontal="true" />
    <WsInput v-model="password" type="password" placeholder="**********"
      >Password</WsInput
    >
    <WsSpace size="l" :horizontal="true" />
    <WsLink href="/reset-password">Forgot password?</WsLink>
    <WsSpace size="l" :scale="1.25" :horizontal="true" />
    <WsButton :disabled="!checkInputs">Sign in</WsButton>
  </div>
</template>

<script>
import WsText from "~/components/WsText";
import WsLink from "~/components/WsLink";
import WsInput from "~/components/WsInput";
import WsButton from "~/components/WsButton";

export default {
  name: "signin",
  components: { WsButton, WsInput, WsLink, WsText },
  data() {
    return {
      email: '',
      password: ''
    };
  },
  computed: {
    checkInputs() {
      return this.email && this.password ? true : false;
    }
  }
};
</script>
