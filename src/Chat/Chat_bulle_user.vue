<template>
<div id="chat-mega-container" style="overflow:auto;">
   <div v-for="message in messagesUser" >
      <div class="chat-friend" style="margin-top:0.2em;">
         <span class="chat-bulle">{{message}}</span>
      </div>
   </div>
</div>
</template>

<script>
export default {
  name: "ChatBulleUser",
  props: ["messagesUser"]
};
</script>

<style>
.chat-bulle-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
.guy {
  margin-left: 0.5em;
  height: 30px;
  border-radius: 50%;
}
.chat-friend {
  display: -webkit-box;
  justify-content: flex-end;
  align-items: center;
  margin-right: 0.6em;
}
.chat-friend > .chat-bulle {
  background-color: #248af8;
  color: white;
  font-weight: 100;
  display: block;
  width: auto;
}
</style>