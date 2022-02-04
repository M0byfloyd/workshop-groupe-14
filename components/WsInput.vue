<template>
    <WsLabel>
      {{ label }}
      <input :type="type">
    </WsLabel>
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
