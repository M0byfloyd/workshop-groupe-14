<template>
  <label>
    <input :type="type" />
  </label>
</template>

<script>
export default {
name: "Input",
  props: {
    type :{ type : String, default : 'text'},
  }
}
</script>

<style scoped>

</style>