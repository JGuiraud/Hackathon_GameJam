<template>
<<<<<<< HEAD
		<div class="chat-friend">
			<span class="chat-bulle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Harum porro exercitationem nostrum quos nemo deleniti natus accusamus commodi eius dignissimos molestiae repudiandae, doloribus neque repellendus sunt vero aliquid necessitatibus, consequuntur in</span>
		</div>
=======
		<ul class="chat-friend" >
			<li class="chat-bulle" v-for="message in messagesUser">{{message}}</li>
		</ul>
>>>>>>> 9a80815817607645963e1525f59cd37fa5fbebef
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
  border-radius: 40%;
}
.chat-friend {
  display: -webkit-box;
  justify-content: flex-end;
  align-items: center;
  margin-right: 0.6em;
}
.chat-friend > .chat-bulle {
  background-color: #f3f3f3;
  color: black;
  display: block;
}
</style>