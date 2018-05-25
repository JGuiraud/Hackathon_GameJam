<template>
	<div>
		<a class="chat_button" href="#" v-for="icon in icons"><i :class="icon.icon"></i></a>
	</div>
</template>

<script>
	export default {
		name: 'ChatInputButton',
		props: ['icons']
	}
</script>

<style>
	.chat_button{
		color:#dedede;
	}
</style>