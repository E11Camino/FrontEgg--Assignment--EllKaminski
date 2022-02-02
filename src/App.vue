<template>
  <div id="app">
    <div v-if="fronteggLoaded">
      <img alt="Vue logo" src="./assets/logo.png" />
      <p>
        Logged in as
        {{ this.authState.user ? this.authState.user.email : "Not logged in" }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      ...this.mapAuthState(),
    };
  },
};
</script>