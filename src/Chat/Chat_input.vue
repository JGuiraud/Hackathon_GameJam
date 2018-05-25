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
          icon: "fas fa-clone"
        },
        {
          name: "add files",
          icon: "add_files"
        },
        {
          name: "add files",
          icon: "far fa-smile"
        },
        {
          name: "add files",
          icon: "fas fa-microphone"
        },
        {
          name: "add files",
          icon: "fas fa-camera"
        },
        {
          name: "add files",
          icon: "far fa-thumbs-up"
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
}
.chat-input {
  /* width: 80vw; */
  margin: 0.5em;
  border: none;
}
</style>