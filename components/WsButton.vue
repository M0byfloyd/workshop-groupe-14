<template>
  <button :type="type">
    <slot>

    </slot>
  </button>
</template>

<script>
export default {
name: "WsButton",
  props: {
    type :{ type : String, required: false}
  }
}
</script>
