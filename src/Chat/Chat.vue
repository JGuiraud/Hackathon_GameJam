<template>
	<div class="col-md-9 chat-container" style="padding:0;">
      <chat-status-bar/>
      <div id="app-chat-bulle-container" class="chat-bulle-container">
         <chat-bulle :listMessages="messages" v-show="messages.length > 0"/>
      <ChatWriting v-show="userIsTyping"/>
      </div>
      <chat-input :parentMessageData="messages" @interface="sayMessage"/>
</div>
      
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
  props: ["finish"],
  data() {
    return {
      userIsTyping: false,
      messages: [],
      isFinish: false
    };
  },
  methods: {
    sayMessage: function(event) {
      var self = this;
      console.log("true ta maman");
      console.log(event);
      if (
        event[event.length - 1].speech == "J'ai entendu parler de le-refuge.org"
      ) {
        console.log("hello");
        setTimeout(function() {
          self.isFinish = true;
          self.$emit("michel", this.isFinish);
        }, 6000);
      }
      self.userIsTyping = true;
      setTimeout(function() {
        self.responseMessage(event);
      }, 3000);
    },

    responseMessage: function(text) {
      var query = text[text.length - 1];
      axios.get(`http://localhost:1337/${query.speech}`).then(res => {
        if (
          query.speech == "pourquoi" ||
          query.speech == "pourquoi ?" ||
          query.speech == "Pourquoi" ||
          query.speach == "Pourquoi ?"
        ) {
          var self = this;
          var splitSpeech = res.data.speech.split(".");
          splitSpeech.map((speech, i) => {
            setTimeout(function() {
              self.messages.push({ user: "bot", speech: speech });
              this.userIsTyping = true;
            }, i * 3000);
            this.userIsTyping = false;
          });
        } else {
          this.messages.push({ user: "bot", speech: res.data.speech });
          this.userIsTyping = false;
        }
      });
    }
  },
  beforeMount() {
    this.isFinish = this.finish;
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