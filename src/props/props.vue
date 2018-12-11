<template>
  <div>
    <div v-for="n in 2" :key="n" style="height:100px; width:100px; background-color:grey;">
      <h1>
        Hello!
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    booked: Boolean,
    appNo: Number
  },
  data () {
    return {
      bananas: {
        color: 'Yellow'
      }
    }
  }
}
</script>
