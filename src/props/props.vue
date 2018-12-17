<template>
  <div style="display:flex; flex-wrap:wrap; align-items:center; margin:5px;">
    <bookingBox v-for="day in 7" :key="day" :id="'dag'+day"></bookingBox>
  </div>
</template>

<script>
import bookingBox from "./bookingbox.vue";
export default {
  name: "Bookings",
  created: function() {
    // console.log(this.$children[0].booked);
    // console.log("Before");
    // for (let i = 0; i < this.$children.length; i++) {
    //   console.log(this.$children[i]);
    // }
    // console.log("After");
    // console.log(this.$children);
    // if (this.appNo !== myAppNo) {
    //   // this.$el.className = "booked";
    //   console.log(this.className);
    // } else if (this.appNo === myAppNo) {
    //   // this.$el.className = "bookedByMe";
    //   console.log(this.className);
    // } else {
    //   // this.$el.className = "free";
    //   console.log(this.className);
    // }
  },
  components: {
    bookingBox
  }
};
</script>
