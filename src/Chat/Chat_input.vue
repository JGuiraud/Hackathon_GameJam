<template>
	<div>
			<div class="col-sm-12 chat-input-container">
				<div>
					<input type="text" v-model="text" @keyup.enter="sendMessage" class="chat-input" placeholder="Type here...">
					{{text}}
				</div>
				<chat-input-button :icons="icons"/>
			</div>
	</div>
</template>

<script>
	import axios from 'axios'
	import	ChatInputButton from "./Chat_input_button"
	export default {
		data(){
			return {
				text: ""
			}
		},
		name: "ChatInput",
		components: {
			ChatInputButton
		},
		methods: {
			sendMessage: function(){
				axios.get(`http://localhost:1337/${this.text}`)
					.then(data => {
						console.log(data)
						this.text = "";
					})
			}
		},
		computed : {
			icons: () => [
					{
						name:"add files",
						icon:"fas fa-clone"
					},
					{
						name:"smiley",
						icon:"far fa-smile"
					},
					{
						name:"vocal message",
						icon:"fas fa-microphone"
					},
					{
						name:"take picture",
						icon:"fas fa-camera"
					},
					{
						name:"Like !",
						icon:"far fa-thumbs-up"
					},
				]
		}
	}
</script>

<style>
.chat-input-container {
  border-top: 1px solid #dedede;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 0.5em;
}
.chat-input {
  width: 55vw;
  height: auto;
  margin: 0.5em;
  border: none;
}
</style>