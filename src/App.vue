<template>
  <div id="app">
    <navbar/>
    <main class="Page-main">
      <div class="Page-container">
        <router-view></router-view>
      </div>
      <Bookings/>
    </main>
    <w-footer/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import WFooter from "./components/WFooter.vue";
import Bookings from "./props/props.vue";
export default {
  name: "app",
  components: {
    Navbar,
    WFooter,
    Bookings
  }
};
</script>

<style lang="less">
@import "src/Assets/Styles/app.less";
</style>

