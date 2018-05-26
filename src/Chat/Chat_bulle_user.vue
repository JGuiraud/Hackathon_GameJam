<template>
		<ul class="chat-friend" >
			<li class="chat-bulle" v-for="message in messagesUser">{{message}}</li>
		</ul>
</template>

<script>
export default {
  name: "ChatBulleUser",
  props: ['messagesUser'],
};
</script>

<style>
.chat-bulle-container {
  /*height: 90vh;*/
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
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin-bottom: 1em;
  margin-right: 0.6em;
}
.chat-friend > .chat-bulle {
  background-color: #ebebeb;
  color: black;
}
</style>