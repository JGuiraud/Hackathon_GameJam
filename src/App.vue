<template>
  <div>
    <navbar/>
    <div class="container-chat-conversation">
      <conversations/>
      <chat/>
    </div>
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
.container-chat-conversation {
  display: flex;
  height: 92vh;
}
</style>
