<template>
  <div class="date unbooked">
    <h1>{{date}}</h1>
  </div>
</template>
<script>
export default {
  props: {
    appNo: {
      type: Number,
      default: null
    },
    booked: {
      type: Boolean,
      default: false
    },
    date: {
      type: Date,
      default: ""
    }
  },
  name: "date"
};
</script>
<style>
.date {
  height: 100px;
  width: calc(100% / 7);
  box-sizing: border-box;
  border: 1px solid white;
  display: flex;
  justify-content: center;
  align-items: center;
}
.unbooked {
  background-color: darkgrey;
  color: white;
}
</style>

