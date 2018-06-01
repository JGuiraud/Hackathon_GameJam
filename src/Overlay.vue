
<template>
   <div class="overlay">
      <div>
      <h1>
         À suivre...
      </h1> 
      </div>
   </div>
</template>
<script>
export default {};
</script>
<style>
.overlay {
  height: 100vh;
  width: 100vw;
  background: rgb(0, 0, 0, 0.9);
  position: fixed;
  z-index: 40000;
}
.overlay > div {
  color: rgb(235, 233, 233);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  opacity: 1;
  transition: opacity 0.3s;
  -webkit-transition: opacity 0.3s;
}
</style>
