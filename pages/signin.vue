<template>
  <main>
    <WsCard>
      <WsTitle>
        Sign In
      </WsTitle>

      <WsText>Not signed-up ? <WsLink href="/signup" >Register</WsLink></WsText>
    </WsCard>

    <WsInput label="Email" type="email"/>

    <WsInput label="Password" type="password"/>

    <WsLink href="/forgot-password">
      Forgot Password ?
    </WsLink>

    <WsButton>
      Sign In
    </WsButton>

  </main>
</template>

<script>
import WsCard from "~/components/WsCard";
import WsTitle from "~/components/WsTitle";
import WsText from "~/components/WsText";
import WsLink from "~/components/WsLink";
import WsInput from "~/components/WsInput";
import WsButton from "~/components/WsButton";
export default {
name: "signin",
  components: {WsButton, WsInput, WsLink, WsText, WsTitle, WsCard}
}
</script>
