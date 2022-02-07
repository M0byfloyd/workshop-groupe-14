<template>
  <div id="check_reset">
    <WsSpace size="m" :horizontal="true" :scale="3" />
    <WsImg
      src="/mail.png"
      alt="Mail image"
      height="150px"
      width="50vw"
      align="center"
    ></WsImg>
    <WsSpace size="s" :horizontal="true" />
    <WsText tag="h1">Check your mail</WsText>
    <WsSpace size="s" :horizontal="true" />
    <WsText tag="small"
      >We have sent a password revover instructions to your email</WsText
    >
    <WsSpace size="m" :horizontal="true" />
    <WsLink href="#"><WsButton>Open your email</WsButton></WsLink>
    <WsSpace size="s" :horizontal="true" />
    <WsLink href="new-password" customStyle="color: var(--color-gray_dark);">Skip</WsLink>
    <WsSpace size="l" :scale="8" :horizontal="true" />
    <WsText tag="small"
      >Did you not receive check your spam filter or
      <WsLink customStyle="color: var(--color-primary)" href="/reset-password">try another email adress</WsLink></WsText
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
import WsImg from "/components/WsImg";

export default {
  name: "reset-password",
  components: {
    WsBackLink,
    WsText,
    WsSpace,
    WsInput,
    WsButton,
    WsLink,
    WsImg,
  },
};
</script>

<style lang="scss" scoped>
#check_reset {
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>
