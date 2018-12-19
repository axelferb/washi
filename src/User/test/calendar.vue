<template>
  <div class="calendar">
    <date v-for="date in daysInMonth" :key="date"></date>
  </div>
</template>
<script>
import date from "./date.vue";

export default {
  name: "calendar",
  components: {
    date
  },
  data() {
    return {
      today: moment(),
      dateContext: moment(),
      displayDate: moment().format("dddd" + " D " + "MMMM"),
      days: ["M", "T", "O", "T", "F", "L", "S"],
      times: [
        "06.00 – 09.00",
        "09.00 – 12.00",
        "12.00 – 15.00",
        "15.00 – 18.00",
        "18.00 – 21.00"
      ],
      selectedDate: "",
      selectedTime: "",
      errorMessage: "",
      successMessage: "",
      bookings: {},
      newBooking: { selectedDate: "", selectedTime: "" },
      clickedUser: {}
    };
  },
  computed: {
    year: function() {
      return this.dateContext.format("Y");
    },
    month: function() {
      return this.dateContext.format("MMMM");
    },
    dayOfMonth: function() {
      return this.dateContext.format("D");
    },
    daysInMonth: function() {
      return this.dateContext.daysInMonth("D");
    },
    currentDate: function() {
      return this.dateContext.get("D");
    },
    firstDayOfMonth: function() {
      const firstDay = moment(this.dateContext).subtract(
        this.currentDate - 1,
        "days"
      );
      return firstDay.weekday();
    },
    initialDate: function() {
      return this.today.get("D");
    },
    initialMonth: function() {
      return this.today.format("MMMM");
    },
    initialYear: function() {
      return this.today.format("Y");
    }
  },
  methods: {
    addMonth: function() {
      this.dateContext = moment(this.dateContext).add(1, "month");
    },
    subtractMonth: function() {
      this.dateContext = moment(this.dateContext).subtract(1, "month");
    },
    setDateId: function(date) {
      const month = this.dateContext.format("MMMM");
      const year = this.dateContext.format("YYYY");
      const day = moment(year + month + date).format("YYYY-MM-DD");
      return day;
    },
    selectDate: function(date) {
      const month = this.dateContext.format("MMMM");
      const year = this.dateContext.format("YYYY");
      const day = moment(year + month + date).format("YYYY-MM-DD");

      this.selectedDate = day;
      this.selectedTime = "";
      this.displayDate = moment(year + month + date).format(
        "dddd" + " D " + "MMMM"
      );
    },
    selectTime: function(time) {
      this.selectedTime = "tid" + time;
      this.newBooking = {
        selectedDate: this.selectedDate,
        selectedTime: "tid" + time
      };
    }
  }
};
</script>
<style>
.calendar {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}
</style>

