<template>
	<div class="chat-bulle-container">
		<div class="chat-friend">
			<span class="chat-bulle">hello world</span>
			<img class="guy" src="../assets/guy.jpg" alt="">
		</div>
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
		justify-content: flex-end;
		flex-direction: column;
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
	.chat-friend{
	}
	.chat-friend>.chat-bulle{
		background-color:rgb(68, 190, 199);
		color:#fff;
	}
</style>