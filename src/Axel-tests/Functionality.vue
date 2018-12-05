<template>
  <div>
    <h1>Log in</h1>
    <form>
      <h2>username</h2>
      <input type="text" placeholder="username">
      <h2>password</h2>
      <input type="password" placeholder="password">
    </form>
    <div>
      <h3>welcome!</h3>
      <p></p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Functionality",
  methods: {
    logIn: function(event) {
      this.loggedInUser.username = usernameInput.value;
      event.preventdefault();
    }
  }
};
</script>
