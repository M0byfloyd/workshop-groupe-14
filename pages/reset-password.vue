<template>
  <div id="reset_password">
    <WsBackLink link="/" :hasArrow="true">Back</WsBackLink>
    <WsSpace size="l" :horizontal="true" :scale="2" />
    <WsText tag="h1">Reset password</WsText>
    <WsSpace size="l" :horizontal="true" :scale="1.5" />
    <WsText tag="p"
      >Enter the email associated with your account and we will send an email
      with instructions to reset your password</WsText
    >
    <WsSpace size="l" :horizontal="true" :scale="1" />
    <WsInput type="email" placeholder="your@mail.com">Email adress</WsInput>
    <WsSpace size="l" :horizontal="true" :scale="1" />
    <WsButton>Confirm</WsButton>
  </div>
</template>

<script>
import WsBackLink from "/components/WsBackLink";
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
  },
};
</script>
