<template>
  <div id="app">
    <div class="Page">
      <section>
        <functionality/>
      </section>
    </div>
  </div>
</template>

<script>
import Mydata from "./Axel-tests/Data.vue";
import Functionality from "./Axel-tests/Functionality.vue";

export default {
  name: "app",
  components: {
    Mydata,
    Functionality
  }
};
</script>

<style lang="less">
body {
  padding: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>

