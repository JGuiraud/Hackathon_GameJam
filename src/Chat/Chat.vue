<template>
	<div class="col-md-9 chat-container" style="padding:0;">
      <chat-status-bar/>
      <div class="chat-bulle-container">
         <chat-bulle/>
<<<<<<< HEAD
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
=======
         <chat-bulle-user :messagesUser="parentMessageData" v-show="parentMessageData.length > 0" />
>>>>>>> 9a80815817607645963e1525f59cd37fa5fbebef
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
import ChatWriting from "./Chat_writing";
export default {
  name: "Chat",
  components: {
    ChatBulle,
    ChatInput,
    ChatBulleUser,
<<<<<<< HEAD
    ChatStatusBar,
    ChatWriting
=======
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
>>>>>>> 9a80815817607645963e1525f59cd37fa5fbebef
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