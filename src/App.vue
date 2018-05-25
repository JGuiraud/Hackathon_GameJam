<template>
  <div>
    <navbar/>

  </div>
</template>

<script>
import Navbar from "./Navbar/Navbar";
import Chat from "./Chat/Chat"
export default {
  name: "App",
  components: {
    Navbar,
    Chat
  }
};
</script>

<style>
</style>
