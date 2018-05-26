<template>
   		<div class="bubble-chat">
			<div class="container-circle">
				<div class="circle cc1" id="circle1"></div>
				<div class="circle cc2" id="circle2"></div>
				<div class="circle cc3" id="circle3"></div>
			</div>
		</div>
</template>
<script>
export default {};
</script>

<style>
.bubble-chat {
  background-color: #e6e7ec;
  width: 140px;
  height: 80px;
  border-radius: 30% / 50%;
  margin: 0 auto;
  position: relative;
  top: 150px;
}

.container-circle {
  width: 100px;
  position: relative;
  margin: 0 auto;
}

.circle {
  height: 20px;
  width: 20px;
  margin: 0 5px;
  background-color: #b6b5ba;
  border-radius: 50%;
  display: inline-block;
  position: relative;
  top: 28px;
  -webkit-animation-duration: 2s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}

#circle1 {
  -webkit-animation-name: circle1;
}

#circle2 {
  -webkit-animation-name: circle2;
}

#circle3 {
  -webkit-animation-name: circle3;
}

#circle1 {
  animation-name: circle1;
}

#circle2 {
  animation-name: circle2;
}

#circle3 {
  animation-name: circle3;
}

.cc1 {
  background-color: #9e9da2;
}

@-webkit-keyframes circle1 {
  0% {
    top: 30px;
  }
  15% {
    top: 20px;
  }
  25% {
    top: 30px;
  }
}

@-webkit-keyframes circle2 {
  10% {
    top: 30px;
  }
  25% {
    top: 20px;
  }
  35% {
    top: 30px;
  }
}

@-webkit-keyframes circle3 {
  15% {
    top: 30px;
  }
  30% {
    top: 20px;
  }
  40% {
    top: 30px;
  }
}

@keyframes circle1 {
  0% {
    top: 30px;
  }
  15% {
    top: 20px;
  }
  25% {
    top: 30px;
  }
}

@keyframes circle2 {
  10% {
    top: 30px;
  }
  25% {
    top: 20px;
  }
  35% {
    top: 30px;
  }
}

@keyframes circle3 {
  15% {
    top: 30px;
  }
  30% {
    top: 20px;
  }
  40% {
    top: 30px;
  }
}
</style>


