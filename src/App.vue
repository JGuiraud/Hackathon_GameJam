<template>
  <div>
   <overlay v-show="finish"/>
    <navbar/>
    <div class="container-chat-conversation">
      <conversations/>
      <chat :finish="finish" @michel="overlay"/>
    </div>
  </div>
</template>

<script>
import Navbar from "./Navbar/Navbar";
import Chat from "./Chat/Chat";
import Conversations from "./Conversations/Conversations";
import Overlay from "./Overlay";
export default {
  name: "App",
  components: {
    Navbar,
    Conversations,
    Chat,
    Overlay
  },
  data() {
    return {
      finish: false
    };
  },
  methods: {
    overlay: function() {
      this.finish = true;
    }
  }
};
</script>

<style>
.container-chat-conversation {
  display: flex;
  height: 92vh;
}
</style>
