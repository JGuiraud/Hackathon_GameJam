<template>
<div class="container-typing">
      <img class="girl-typing" src="../assets/guy2.jpeg" alt="">
   <div class="fb-chat">
      <div class="fb-chat--bubbles">
         <span></span>
         <span></span>
         <span></span>
      </div>
   </div>
</div>
</template>
<script>
export default {};
</script>

<style>
.container-typing {
  display: flex;
  align-items: center;
  margin-top: 0.2em;
  margin-bottom: 0.2em;
}
.container-typing > .girl-typing {
  margin-left: 1.1em;
  height: 30px;
  border-radius: 50%;
}
.fb-chat {
  background-color: #f3f3f3;
  width: 50px;
  line-height: 30px;
  border-radius: 30%/50%;
  margin-left: 3.7em;
  transform: translate(-0%, -0%);
  height: 1.9em;
  margin-left: 0.7em;
}
.fb-chat--bubbles {
  text-align: center;
}
.fb-chat--bubbles span {
  display: inline-block;
  background-color: #d4d4d4;
  width: 6px;
  height: 6px;
  border-radius: 100%;
  animation: bob 2s infinite;
  margin-bottom: 0.1em;
  margin-right: -0.07em;
}
.fb-chat--bubbles span:nth-child(2) {
  animation-delay: 0.15s;
}
.fb-chat--bubbles span:nth-child(3) {
  animation-delay: 0.3s;
}

@keyframes bob {
  10% {
    transform: translateY(-4px);
    background-color: #838383;
  }
  50% {
    transform: translateY(0);
    background-color: #bbbbbb;
  }
}
</style>


