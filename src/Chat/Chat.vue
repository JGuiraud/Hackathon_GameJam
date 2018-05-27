<template>
	<div class="col-md-9 chat-container" style="padding:0;">
      <chat-status-bar/>
      <div id="app-chat-bulle-container" class="chat-bulle-container">
         <!-- <chat-bulle-user :messagesUser="parentMessageData" v-show="parentMessageData.length > 0" /> -->
         <chat-bulle :listMessages="messages" v-show="messages.length > 0"/>
      <ChatWriting v-show="userIsTyping"/>
      </div>
      <chat-input :parentMessageData="messages" @interface="sayMessage"/>
   </div>
      
	<!-- </div> -->
</template>

<script>
import axios from "axios";

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
  },
  data() {
    return {
      userIsTyping: false,
      messages: []
    };
  },
  methods: {
    sayMessage:function(event) {
      var self = this;
      self.userIsTyping = true
      setTimeout(function(){self.responseMessage(event)}, 3000);
    },
    responseMessage: function(text) {

      var query = text[text.length - 1];
      axios.get(`http://localhost:1337/${query.speech}`).then(res => {
        this.messages.push({ user: "bot", speech: res.data.speech });
        this.userIsTyping = false;
      });
    }
  },
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