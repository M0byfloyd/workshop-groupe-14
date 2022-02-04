<template>
  <button :type="type" />
</template>

<script>
export default {
name: "WsButton",
  type :{ type : String, required: false}
}
</script>
