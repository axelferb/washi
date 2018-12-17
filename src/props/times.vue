<template>
  <p>Tid</p>
</template>
<script>
export default {
  name: "timeBox",
  props: {
    booking: {
      date: {
        type: Date,
        default: ""
      },
      time: {
        type: String,
        default: undefined
      },
      appNo: {
        type: Number,
        default: null
      }
    }
  }
};
</script>
<style>
#tid1 {
  color: red;
}
</style>


