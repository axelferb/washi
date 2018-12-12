<template>
  <div style="display:flex; justify-content:center; align-items:center; margin:15px; auto;">
    <div class="Loopers" v-for="n in 5" :key="n" style="display:flex; justify-content:center; align-items:center; height:100px; width:100px; background-color:grey; box-sizing:border-box; border:1px solid white;">
      <p>
        {{this.$props}}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    booked: 'Hello!',
    appNo: String
  },
  data () {
    return {

      }
  },
  methods: {
    book: function (event) {
      }
  },
  created: function() {
    console.log(this.$props + 'Hello!')
    console.log(this.$props.booked)
  }
}
</script>
