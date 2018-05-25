<template>
	<div class="col-md-9 chat-container" style="padding:0;">
		<chat-bulle/>
		<chat-input/>
	</div>
</template>

<script>
import ChatBulle from "./Chat_bulle";
import ChatInput from "./Chat_input";
export default {
  name: "Chat",
  components: {
    ChatBulle,
    ChatInput
  }
};
</script>

<style>
.chat-container {
  padding: 0;
  display: flex;
  flex-direction: column;
}
</style>