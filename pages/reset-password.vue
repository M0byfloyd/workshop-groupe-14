<template>
  <div id="reset_password">
    <WsBackLink link="/" :hasArrow="true">Back</WsBackLink>
    <WsText tag="h1">Reset password</WsText>
    <WsText tag="p"
      >Enter the email associated with your account and we will send an email
      with instructions to reset your password</WsText
    >
    <WsInput label="Email adress"></WsInput>
    <WsButton>Confirm</WsButton>
  </div>
</template>

<script>
import WsBackLink from "/components/WsBackLink";
import WsText from "/components/WsText";
import WsInput from "/components/WsInput";
import WsButton from "/components/WsButton";

export default {
  name: "reset-password",
  components: {
    WsBackLink,
    WsText,
    WsInput,
    WsButton,
  },
};
</script>
