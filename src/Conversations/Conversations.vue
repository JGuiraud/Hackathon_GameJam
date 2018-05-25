<template>
	<div class="col-md-3 conversation-mega-container">
      <conversationsStatusBar/>
   </div>
</template>

<script>
import ConversationsStatusBar from "./ConversationsStatusBar";
export default {
  name: "Conversations",
  components: {
    ConversationsStatusBar
  }
};
</script>

<style>
.conversation-mega-container {
  height: 93vh;
  padding: 0;
  border-right: 1px solid lightgray;
}
</style>