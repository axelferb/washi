<template>
  <div>
    <button v-on:click="changeText">
      {{users[0].username}}
    </button>
  </div>
</template>

<script>
  export default {
    methods: {
      changeText: function(event) {
        this.users[0].username = 'kuken'
      }
    },
    name: "testData",
    data() {
      // console.log(this)
      return {
        users: [
          {
            username: "user1",
            password: "pass1",
            appNo: 1301
          },
          {
            username: "user2",
            password: "pass2",
            appNo: 1302
          },
          {
            username: "user3",
            password: "pass3",
            appNo: 1303
          }
        ]
      }
    }
  }
</script>