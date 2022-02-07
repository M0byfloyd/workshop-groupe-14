<template>
  <div id="reset_password">
    <WsBackLink link="/" :hasArrow="true">Back</WsBackLink>
    <WsSpace size="l" :horizontal="true" :scale="2" />
    <WsText tag="h1">Reset password</WsText>
    <WsSpace size="l" :horizontal="true" :scale="1.5" />
    <WsText tag="p"
      >Enter the email associated with your account and we will send an email
      with instructions to reset your password.</WsText
    >
    <WsSpace size="l" :horizontal="true" :scale="1" />
    <WsInput v-model="email" type="email" placeholder="your@mail.com"
      >Email address</WsInput
    >
    <WsSpace size="l" :horizontal="true" :scale="1" />
    <WsLink :disabled="!checkPasswords" href="/reset-password/check-mail"
      ><WsButton :disabled="!checkPasswords">Confirm</WsButton></WsLink
    >
  </div>
</template>

<script>
import WsBackLink from "/components/WsBackLink";
import WsLink from "/components/WsLink";
import WsText from "/components/WsText";
import WsInput from "/components/WsInput";
import WsButton from "/components/WsButton";
import WsSpace from "/components/WsSpace";

export default {
  name: "reset-password",
  components: {
    WsBackLink,
    WsText,
    WsSpace,
    WsInput,
    WsButton,
    WsLink,
  },
  data() {
    return {
      email: "",
    };
  },
  computed: {
    checkPasswords() {
      return this.email ? true : false;
    },
  },
};
</script>
