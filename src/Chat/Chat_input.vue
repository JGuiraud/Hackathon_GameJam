<template>
	<div>
			<div class="col-sm-12 chat-input-container">
				<div>
					<input type="text" class="chat-input" placeholder="Type here...">
				</div>
				<chat-input-button :icons="icons"/>
			</div>
	</div>
</template>

<script>
import ChatInputButton from "./Chat_input_button";
export default {
  name: "ChatInput",
  components: {
    ChatInputButton
  },
  computed: {
    icons: function() {
      const icons = [
        {
          name: "add files",
          icon: "fas fa-clone",
          color: "blue"
        },
        {
          name: "smiley",
          icon: "far fa-smile",
          color: "blue"
        },
        {
          name: "vocal message",
          icon: "fas fa-microphone",
          color: "blue"
        },
        {
          name: "take picture",
          icon: "fas fa-camera",
          color: "blue"
        },
        {
          name: "Like !",
          icon: "far fa-thumbs-up",
          color: "blue"
        }
      ];
      return icons;
    }
  }
};
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