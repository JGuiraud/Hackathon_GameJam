<template>
  <div>
    <navbar/>
    <conversations/>
    <chat/>
  </div>
</template>

<script>
import Navbar from "./Navbar/Navbar";
import Chat from "./Chat/Chat";
import Conversations from "./Conversations/Conversations";
export default {
  name: "App",
  components: {
    Navbar,
    Conversations,
    Chat
  }
};
</script>

<style>
</style>
