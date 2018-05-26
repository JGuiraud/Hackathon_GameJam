<template>
		<div class="chat-friend">
			<span class="chat-bulle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Harum porro exercitationem nostrum quos nemo deleniti natus accusamus commodi eius dignissimos molestiae repudiandae, doloribus neque repellendus sunt vero aliquid necessitatibus, consequuntur in</span>
		</div>
</template>

<script>
export default {
  name: "ChatBulleUser"
};
</script>

<style>
.chat-bulle-container {
  height: 90vh;
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