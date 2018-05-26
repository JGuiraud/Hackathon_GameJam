<template>
	<div class="col-md-9 chat-container" style="padding:0;">
      <chat-status-bar/>
      <div class="chat-bulle-container">
         <chat-bulle-user :messagesUser="parentMessageData" v-show="parentMessageData.length > 0" />
         <chat-bulle :responseMessage="response" v-show="response.length > 0"/>
      </div>
      <ChatWriting/>
      <chat-input :parentMessageData=parentMessageData @interface="sayMessage"/>
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
      parentMessageData: [],
      messages: [],
      response: []
    };
  },
  methods: {
    sayMessage: function(event){
      this.responseMessage(event)
    },
    responseMessage: function(text){
      var query = text[text.length-1]
      axios.get(`http://localhost:1337/${query}`).then(res => {
        this.response.push(res.data);
      });
    }
  },
  computed: {
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