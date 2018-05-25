<template>
	<div>
		<chat-bulle/>
		<chat-input/>
	</div>
</template>

<script>
	import	ChatBulle from "./Chat_bulle"
	import ChatInput from "./Chat_input"
	export default {
		name: "Chat",
		components: {
			ChatBulle,
			ChatInput,
		}
	}
</script>

<style>
	
</style>