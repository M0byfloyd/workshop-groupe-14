<template>
  <label>
    <WsLabel>
      {{ label }}
    </WsLabel>
    <input :type="type">
  </label>
</template>

<script>
import WsLabel from "~/components/WsLabel";
export default {
name: "WsInput",
  components: {WsLabel},
  type: { type : String, default : 'text'},
  label: { type : String, required: true}
}
</script>
