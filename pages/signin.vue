<template>
  <main>
    <WsCard>
      <WsText :tag="h1">
        Sign In
      </WsText>

      <WsText>Not signed-up? <WsLink href="/signup" >Register</WsLink></WsText>
    </WsCard>

    <WsInput label="Email" type="email"/>

    <WsInput label="Password" type="password"/>

    <WsLink href="/forgot-password">
      Forgot password ?
    </WsLink>

    <WsButton>
      Sign in
    </WsButton>
  </main>
</template>

<script>
import WsCard from "~/components/WsCard";
import WsText from "~/components/WsText";
import WsLink from "~/components/WsLink";
import WsInput from "~/components/WsInput";
import WsButton from "~/components/WsButton";

export default {
name: "signin",
  components: {WsButton, WsInput, WsLink, WsText, WsCard}
}
</script>
