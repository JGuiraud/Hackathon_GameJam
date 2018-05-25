<template>
		<div class="chat-user">
			<img class="guy" src="../assets/girl.jpeg" alt="">
			<span class="chat-bulle chat-bulle-user">hello world</span>
		</div>
</template>

<script>
export default {
  name: "ChatBulle"
};
</script>

<style>
.chat-bulle-container {
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
.chat-user {
  margin-left: 0.6em;
  margin-top: 0.1em;
  /*flex-grow: 1;*/
}
.chat-bulle {
  /* padding: 0.5em; */
  padding-top: 0.3em;
  padding-bottom: 0.3em;
  padding-left: 1em;
  padding-right: 1em;
  border-radius: 30px;
  color: rgb(24, 24, 24);
  font-size: 14px;
  width: 80%;
}
.chat-bulle-user {
  color: white;
  background-color: #1787fb;
}
.guy {
  margin-right: 0.5em;
  height: 30px;
  border-radius: 50%;
}
</style>