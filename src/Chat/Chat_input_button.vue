<template>
	<div class="chat-container-button">
		<i v-for="icon in icons" v-bind:class="icon.icon"></i>
	</div>
</template>

<script>
export default {
  name: "ChatInputButton",
  props: ["icons"]
};
</script>

<style>
.chat-container-button {
  padding: 0.5em;
  display: flex;
  align-items: center;
}

.chat-container-button > i {
  font-size: 20px;
  padding-left: 10px;
  color: lightgrey;
}
</style>