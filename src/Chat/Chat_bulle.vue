<template>
<div>
  <ul class="merde">
      <li class="chat-user" v-for="message in listMessages">
        <img v-show="message.user === 'bot'" class="guy" src="../assets/girl.jpeg" alt="">
        <span :class="{human: message.user == 'human'}" class="chat-bulle chat-bulle-user" >{{message.speech}}</span>
      </li>
  </ul>
</div>
</template>

<script>
export default {
  name: "ChatBulle",
  props: ["listMessages"]
};
</script>

<style>
.merde {
  padding-left: 1em;
  padding-right: 1em;
}
.chat-bulle-container {
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
.chat-bulle-container > div {
  overflow: scroll;
}
.chat-user {
  margin-bottom: 0.7em;
}

.chat-bulle {
  padding-top: 0.3em;
  padding-bottom: 0.3em;
  padding-left: 1em;
  padding-right: 1em;
  border-radius: 30px;
  color: rgb(24, 24, 24);
  font-size: 14px;
  width: 80%;
  height: 2.25em;
}
.chat-bulle-user {
  color: rgb(32, 32, 32);
  background-color: #f3f3f3;
  padding-top: 0.5em;
  padding-bottom: 0.5em;
  font-weight: 200;
  width: auto;
  display: inline-table;
}
.guy {
  margin-right: 0.5em;
  height: 30px;
  border-radius: 50%;
}
ul {
  color: white !important;
}

.chat-user > .human {
  background-color: #248af8 !important;
  color: white;
  font-weight: 100;
  width: auto;
  float: right;
  padding-top: 5px;
}
</style>