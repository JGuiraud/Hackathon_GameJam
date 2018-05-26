<template>
		<div class="chat-user">
			<img class="guy" src="../assets/girl.jpeg" alt="">
			<span class="chat-bulle chat-bulle-user" >hello world</span>
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
  margin-top: 0em;
}
.chat-bulle {
  padding-top: 0.3em;
  padding-bottom: 0.3em;
  padding-left: 1em;
  padding-right: 1em;
  border-radius: 30px;
  color: rgb(24, 24, 24);
  font-size: 14px;
  width: 80%;
  height: 2.25em;
}
.chat-bulle-user {
  color: rgb(32, 32, 32);
  background-color: #f3f3f3;
  padding-top: 0.5em;
  padding-bottom: 0.5em;
  font-weight: 200;
}
.guy {
  margin-right: 0.5em;
  height: 30px;
  border-radius: 50%;
}
</style>