<template>
	<div>
			<div class="col-sm-12 chat-input-container">
				<div>
					<input type="text" v-model="text" @keyup.enter="sendMessage" class="chat-input" placeholder="Écrivez un message...">
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
  props: {
    parentMessageData: {
      type: Array,
      default() {
        return "";
      }
    }
  },
  data() {
    return {
      text: "",
      messages: []
    };
  },
  methods: {
    sendMessage: function() {
      this.messages.push({ user: "human", speech: this.text });
      this.text = "";
      this.$emit("interface", this.messages);
    }
  },
  beforeMount() {
    this.messages = this.parentMessageData;
  },
  computed: {
    icons: () => [
      {
        name: "add files",
        icon: "fas fa-clone"
      },
      {
        name: "smiley",
        icon: "far fa-smile"
      },
      {
        name: "vocal message",
        icon: "fas fa-microphone"
      },
      {
        name: "take picture",
        icon: "fas fa-camera"
      },
      {
        name: "Like !",
        icon: "far fa-thumbs-up"
      }
    ]
  }
};
</script>

<style>
.chat-input-container {
  border-top: 1px solid #dedede;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  /* margin-top: 0.2em; */
}
.chat-input {
  width: 55vw;
  height: auto;
  margin-top: 0.7em;
  border: none;
  font-size: 14px;
}

.chat-input:focus {
  outline: none;
}
</style>