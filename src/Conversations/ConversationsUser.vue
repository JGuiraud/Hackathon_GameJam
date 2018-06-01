<template>
	<div>
      <div v-for="user in users" class="user-card">
         <div class="photo">
            <img :src="user.picture" alt="">
         </div>
         <div class="resume-conversation">
            <p>{{user.name}}</p>
            <p>{{user.conversation}}</p>
         </div>
         <div class="time">
            {{user.date}}
         </div>
      </div>
   </div>
</template>


<script>
export default {
  props: ["users"]
};
</script>


<style>
.user-card {
  display: flex;
  flex-direction: row;
  padding-top: 7px;
  padding-bottom: 7px;
  padding-left: 10px;
}
.user-card > .resume-conversation {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding-left: 10px;
}
.user-card > .time {
  display: flex;
  align-items: flex-start;
  justify-content: flex-end;
  flex-grow: 1;
  padding-right: 10px;
  padding-top: 7px;
  color: rgb(180, 179, 179);
  font-size: 14px;
  font-weight: 100;
}
.user-card > .resume-conversation > p {
  margin: 0;
  font-weight: 100;
}
.user-card > .resume-conversation > p:nth-child(2) {
  font-size: 14px;
  color: rgb(180, 179, 179);
}
.user-card > .photo > img {
  height: 60px;
  width: 60px;
  border-radius: 50%;
}
</style>