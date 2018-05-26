<template>
<div class="fb-chat">
  <div class="fb-chat--bubbles">
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>
</template>
<script>
export default {};
</script>

<style>
.fb-chat {
  background-color: #248af8;
  width: 40px;
  line-height: 25px;
  border-radius: 30%/50%;
  margin-left: 3.7em;
  margin-top: 0.2em;
  transform: translate(-0%, -0%);
}
.fb-chat--bubbles {
  text-align: center;
}
.fb-chat--bubbles span {
  display: inline-block;
  background-color: #f7f7f7;
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
    background-color: #d6d6d6;
  }
  50% {
    transform: translateY(0);
    background-color: #f7f7f7;
  }
}
</style>


