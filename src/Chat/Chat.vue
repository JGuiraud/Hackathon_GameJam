<template>
	<div class="col-md-9 chat-container" style="padding:0;">
      <chat-status-bar/>
      <div class="chat-bulle-container">
         <chat-bulle/>
         <chat-bulle />
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
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle/>
         <chat-bulle-user/>
     
         
         <div class="waiting-area">
            <chat-writing/>
         </div>
      </div>
      <chat-input/>
   </div>
      
	<!-- </div> -->
</template>

<script>
import ChatBulle from "./Chat_bulle";
import ChatBulleUser from "./Chat_bulle_user";
import ChatInput from "./Chat_input";
import ChatStatusBar from "./Chat_status_bar";
import ChatWriting from "./Chat_writing";
export default {
  name: "Chat",
  components: {
    ChatBulle,
    ChatInput,
    ChatBulleUser,
    ChatStatusBar,
    ChatWriting
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