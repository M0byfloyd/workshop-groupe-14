<template>
  <div id="app">
    <WsCard>
      <WsTitle>
        Login
      </WsTitle>

      <WsInput />

    </WsCard>
  </div>
</template>

<script>
import WsCard from "./components/WsCard";
import WsTitle from "./components/WsTitle";
import WsInput from "./components/WsInput";

export default {
  name: 'App',
  components: {
    WsCard,
    WsInput,
    WsTitle
  }
}
</script>
