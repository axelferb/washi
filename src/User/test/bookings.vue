<template>
  <div class="bookings">
    <calendar></calendar>
  </div>
</template>
<script>
import calendar from "./calendar.vue";

export default {
  name: "bookings",
  components: {
    calendar
  }
};
</script>
