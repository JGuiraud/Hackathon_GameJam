<template>
		<div class="chat-friend">
			<span class="chat-bulle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Harum porro exercitationem nostrum quos nemo deleniti natus accusamus commodi eius dignissimos molestiae repudiandae, doloribus neque repellendus sunt vero aliquid necessitatibus, consequuntur inventore. Optio eligendi quo natus tempore, quam iure, cupiditate deleniti, numquam quia eum modi veniam beatae! Cupiditate maiores, veritatis placeat optio tempore tenetur odio perferendis eius, eaque facere ex repudiandae. Fuga voluptate nobis delectus ab accusamus iste et, eius, blanditiis ratione commodi earum debitis magnam maxime porro quam error perspiciatis. Facere ut consectetur laboriosam eveniet numquam aliquid, exercitationem illum eaque neque reprehenderit minima magni a tempora reiciendis, debitis qui. Et.</span>
		</div>
</template>

<script>
export default {
  name: "ChatBulleUser"
};
</script>

<style>
.chat-bulle-container {
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
.guy {
  margin-left: 0.5em;
  height: 30px;
  border-radius: 50%;
}
.chat-friend {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin-bottom: 1em;
  margin-right: 0.6em;
}
.chat-friend > .chat-bulle {
  background-color: #f3f3f3;
  color: black;
}
</style>