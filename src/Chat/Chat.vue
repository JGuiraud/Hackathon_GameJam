<template>
	<div class="col-md-9 chat-container" style="padding:0;">
         <div class="chat-bulle-container">
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
            <chat-bulle/>
         </div>
      <chat-input/>
   </div>
      
	<!-- </div> -->
</template>

<script>
import ChatBulle from "./Chat_bulle";
import ChatInput from "./Chat_input";
export default {
  name: "Chat",
  components: {
    ChatBulle,
    ChatInput
  }
};
</script>

<style>
.chat-container {
  padding: 0;
  display: flex;
  flex-direction: column;
}

.chat-bulle-container {
  overflow: scroll;
  height: 100px;
}
</style>