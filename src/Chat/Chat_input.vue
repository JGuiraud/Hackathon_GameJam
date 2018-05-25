<template>
	<div class="container">
			<div class="col-sm-12 chat-container">
				<div>
					<input type="text" class="chat-input" placeholder="Type here...">
				</div>
				<chat-input-button :icons="icons"/>
			</div>
	</div>
</template>

<script>
	import	ChatInputButton from "./Chat_input_button"
	export default {
		name: "ChatInput",
		components: {
			ChatInputButton
		},
		computed : {
			icons: function() {
				const icons = [
					{
						name:"add files",
						icon:"fas fa-copy"
					},
					{
						name:"add files",
						icon:"add_files"
					},
					{
						name:"add files",
						icon:"add_files"
					},
					{
						name:"add files",
						icon:"add_files"
					},
					{
						name:"add files",
						icon:"add_files"
					},
					{
						name:"add files",
						icon:"add_files"
					},
				]
				return icons;
			}
		}
	}
</script>

<style>
	.chat-container{
		border-top: 1px solid #DEDEDE;
		display: flex;
		flex-direction: row;
	}
	.chat-input{
		margin: 0.5em;
		border: none;
	}
</style>