<template>
<div>
   <div class="conversations-status-bar col-md-12 row">
      <div class="col-md-2 logo-left"><i class="fab fa-whmcs"></i></div>
      <div class="col-md-8 title">Messenger</div>
      <div class="col-md-2 logo-right"><i class="fas fa-pencil-alt"></i></div>
   </div>
   <div class="conversations-users">
      <conversationsUser :users="users"/>
   </div>
</div>
</template>

<script>
import ConversationsUser from "./ConversationsUser";
export default {
  name: "ConversationsStatusBar",
  components: {
    ConversationsUser
  },
  computed: {
    users: () => [
      {
        picture: "/static/img/guy2.jpeg",
        name: "Gage Burnett",
        conversation: "Salut !",
        date: "Actif"
      },
      {
        picture: "/static/img/girl.jpeg",
        name: "Esma Seldin",
        conversation: ":*",
        date: "Ven"
      },
      {
        picture: "/static/img/guy3.jpeg",
        name: "Christopher Ball",
        conversation: "Ponctuation ne régit les Bol...",
        date: "Ven"
      },
      {
        picture: "/static/img/girl2.jpeg",
        name: "Alyson Mcknight",
        conversation: "Le grand Oxymore voulut...",
        date: "Sam"
      },
      {
        picture: "/static/img/girl3.jpeg",
        name: "Emily Mills",
        conversation: "Mais ces mots ne firent écho...",
        date: "Sam"
      },
      {
        picture: "/static/img/girl4.jpeg",
        name: "Scarlett Smith",
        conversation: "Alors qu'il avait gravi les...",
        date: "Sam"
      },
      {
        picture: "/static/img/guy4.jpeg",
        name: "Valentino Barlow",
        conversation: ":)",
        date: "Dim"
      },
      {
        picture: "/static/img/guy6.jpeg",
        name: "Daniel May",
        conversation: "A la prochaine !",
        date: "Dim"
      },
      {
        picture: "/static/img/guy5.jpeg",
        name: "Pedro Lucas",
        conversation: "Je suis oublié dans cette messagerie...",
        date: "Dim"
      },
      {
        picture: "/static/img/guy7.jpeg",
        name: "Boby June",
        conversation: "Moi aussi, je suis oublié.. :(",
        date: "Dim"
      },
      {
        picture: "/static/img/guy8.jpeg",
        name: "Lucas Perreira",
        conversation: "Personne ne nous répond",
        date: "Dim"
      }
    ]
  }
};
</script>

<style>
.conversations-users {
  height: 86vh;
  overflow: scroll;
}

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
  color: #375188;
}
.conversations-status-bar > .logo-left {
  padding-left: 0;
}
.conversations-status-bar > .logo-right {
  padding-right: 0;
}
</style>
