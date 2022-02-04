<template>
    <WsText :tag="label">
      {{ label }}
      <input :type="type">
    </WsText>
</template>

<script>
import WsLabel from "~/components/WsLabel";
export default {
name: "WsInput",
  components: {WsLabel},
  props :{
    type: { type : String, default : 'text'},
    label: { type : String, required: true}
  }
}
</script>
