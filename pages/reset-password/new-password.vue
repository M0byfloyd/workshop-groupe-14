<template>
  <div id="new-password">
    <WsBackLink link="/" :hasArrow="true">Back</WsBackLink>
    <WsSpace size="l" :horizontal="true" :scale="2" />
    <WsText tag="h1">New password</WsText>
    <WsSpace size="l" :horizontal="true" :scale="1.5" />
    <WsText tag="p"
      >Your new password must be different from previous used password</WsText
    >
    <WsSpace size="l" :horizontal="true" :scale="1" />
    <!-- <WsInput type="email" placeholder="your@mail.com">Email adress</WsInput> -->
    <WsText tag="p"
      >New Password</WsText
    >
    <WsInput placeholder="********" label="Password" type="password"/>
    <WsSpace size="m" :horizontal="true" :scale="1" />
    <WsText tag="p"
      >Confirm Password</WsText
    >
    <WsInput placeholder="********" label="Password" type="password"/>
    <WsSpace size="s" :horizontal="true" :scale="2" />
    <WsLink href="/signin"><WsButton>Confirm</WsButton></WsLink>
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
  name: "new-password",
  components: {
    WsBackLink,
    WsText,
    WsSpace,
    WsInput,
    WsButton,
    WsLink,
  },
};
</script>
