<template>
<div>
   <div class="conversations-status-bar col-md-12 row">
      <div class="col-md-2 logo-left"><i class="fab fa-whmcs"></i></div>
      <div class="col-md-8 title">Messenger</div>
      <div class="col-md-2 logo-right"><i class="fas fa-pencil-alt"></i></div>
   </div>
   <div class="conversations-users">
      <conversationsUser/>
      <conversationsUser/>
      <conversationsUser/>
      <conversationsUser/>
   </div>
</div>
</template>

<script>
import ConversationsUser from "./ConversationsUser";
export default {
  name: "ConversationsStatusBar",
  components: {
    ConversationsUser
  }
};
</script>

<style>
.conversations-status-bar {
  height: 50px;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: 1px solid rgb(226, 226, 226);
}

.conversations-status-bar > .title,
.logo-left,
.logo-right {
  display: flex;
  justify-content: center;
}

.conversations-status-bar > .logo-left,
.logo-right {
  font-size: 25px;
  color: #4768af;
}
</style>
