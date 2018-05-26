<template>
	<div class="chat-status-bar">
      <div class="empty"></div>
      <div class="chat-status-bar-name">
         <p>Jean Bon</p>
         <p>Actif Maintenant</p>
      </div>
      <div class="action-buttons-chat">
         <i class="fas fa-phone"></i>
         <i class="fas fa-video"></i>
         <i class="fas fa-info-circle"></i>
      </div>
   </div>
</template>

<script>
export default {};
</script>

<style>
.chat-status-bar {
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid rgb(226, 226, 226);
  position: fixed;
  height: 50px;
  width: 75vw;
  display: inline-flex;
  background: white;
}
.chat-status-bar > .chat-status-bar-name {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.chat-status-bar > .chat-status-bar-name > p {
  margin: 0;
  font-weight: 100;
}
.chat-status-bar > .chat-status-bar-name > p:nth-child(2) {
  font-size: 14px;
  color: rgb(180, 179, 179);
}
.chat-status-bar > .action-buttons-chat {
  width: 8vw;
  display: flex;
  justify-content: space-around;
  padding-right: 1em;
}
.chat-status-bar > .action-buttons-chat > i:nth-child(1) {
  transform: rotate(90deg);
  font-size: 23px;
  color: #375188;
}
.chat-status-bar > .action-buttons-chat > i:nth-child(2) {
  font-size: 23px;
  padding-right: 0.8em;
  padding-left: 0.8em;
  color: #375188;
}
.chat-status-bar > .action-buttons-chat > i:nth-child(3) {
  font-size: 23px;
  color: #375188;
  margin-right: 0.9em;
}
</style>