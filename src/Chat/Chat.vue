<template>
	<div class="col-md-9 chat-container" style="padding:0;">
      <chat-status-bar/>
      <div class="chat-bulle-container">
         <chat-bulle/>
         <chat-bulle-user :messagesUser="parentMessageData" v-show="parentMessageData.length > 0" />
      </div>
      <chat-input :parentMessageData=parentMessageData @interface="sayMessage"/>
   </div>
      
	<!-- </div> -->
</template>

<script>
import ChatBulle from "./Chat_bulle";
import ChatBulleUser from "./Chat_bulle_user";
import ChatInput from "./Chat_input";
import ChatStatusBar from "./Chat_status_bar";
export default {
  name: "Chat",
  components: {
    ChatBulle,
    ChatInput,
    ChatBulleUser,
    ChatStatusBar
  },
  data(){
    return{
      parentMessageData: [],
      messages: [],
    }
  },
  methods: {
    sayMessage: (event) => {
      console.log(event)
      this.messages = event
    },
  },
  computed: {
    responseMessage: () => {
      axios.get(`http://localhost:1337/${this.text}`)
          .then(res => {
            this.response =  res.data
      })
    }
  }
}
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