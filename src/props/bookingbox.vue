<template>
  <div class="free" @click="bookMe" style="margin: 5px; padding: 5px; outline:1px solid black;">
    <p>Dag</p>
    <hr>
    <timeBox v-for="time in 5" :key="time" :id="'tid'+time"></timeBox>
  </div>
</template>
<script>
import timeBox from "./times.vue";
var myAppNo = 1337;
export default {
  created: function() {
    console.log(this);
  },
  name: "bookingBox",
  methods: {
    bookMe: function() {
      // console.log(this.$el.className);
      // if (this.booked === false) {
      //   this.booked = true;
      //   this.appNo = myAppNo;
      //   this.bookDate = new Date();
      // } else if (this.appNo !== myAppNo) {
      //   alert("Den här tiden är redan bokad av " + this.appNo);
      // } else if (this.appNo === myAppNo) {
      //   alert("Du har redan bokat den här tiden");
      // }
    }
  },
  props: {
    date: {
      type: Date,
      default: "2011-01-01"
    }
  },
  components: {
    timeBox
  }
};
</script>
<style>
.free {
  background-color: grey;
}
.booked {
  background-color: red;
}
.bookedByMe {
  background-color: green;
}
</style>

