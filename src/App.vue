<template>
  <div id="app">
    <navbar/>
    <main class="Page-main">
      <div class="Page-container">
        <!-- <router-view></router-view> -->
      </div>
      <props/>
    </main>
    <w-footer/>
  </div>
</template>

<script>
// console.log(props.data)
import Navbar from './components/Navbar.vue';
import WFooter from './components/WFooter.vue';
import Props from './props/props.vue';
console.log(Props.props)
export default {
  name: 'app',
  components: {
    Navbar,
    WFooter,
    Props
  }
}
</script>

<style lang="less">
  @import 'src/Assets/Styles/app.less';
</style>

