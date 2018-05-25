<template>
	<div class="chat-bulle-container">
		<div class="chat-user">
			<img class="guy" src="../assets/guy.jpg" alt="">
			<span class="chat-bulle">hello world</span>
		</div>
	</div>
</template>

<script>
	export default {
		name: "ChatBulle"
	}
</script>

<style>
	.chat-bulle-container{
		height: 84vh;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
	}
	.chat-user{
		margin-bottom: 1em;
		margin-left: .6em;
		/*flex-grow: 1;*/
	}
	.chat-bulle{
		background-color: #DEDEDE;
		padding: .5em;
		border-radius: 10px;
	}
	.guy {
		margin-right: .5em;
  	height: 30px;
  	border-radius: 50%;
	}
</style>