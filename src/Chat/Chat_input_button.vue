<template>
	<div class="chat-container-button">
		<a class="chat-button" href="#" v-for="icon in icons"><i :class="icon.icon"></i></a>
	</div>
</template>

<script>
	export default {
		name: 'ChatInputButton',
		props: ['icons']
	}
</script>

<style>
	.chat-container-button{
		padding: .5em;
	}
	.chat-button{
		color:#dedede;
		padding: 2px;
	}
</style>