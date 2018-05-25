<template>
   <div class="container-fluid navbar">
      <div class="container">
         <div class="navbar-left">
            <i class="fab fa-facebook fa-2x"></i>
            <div class="input-group ml-2 mr-sm-2 search-input">
               <input type="text" class="form-control" id="inlineFormInputGroupUsername2" placeholder="Rechercher" style="width:400px;">
               <div class="input-group-prepend">
                  <div class="input-group-text search-navbar"><i class="fas fa-search"></i></div>
               </div>
            </div>
         </div>
         <div class="navbar-right">
            <div class="id">
               <img mr-0 class="guy" src="../assets/guy.jpg" alt="">
               <p>Nico</p>
               </div>
            <div class="accueil">
               <p>
                  Accueil
               </p>
            </div>
            <div>
               <i class="fas fa-user"></i>
               <i class="fas fa-user"></i>
               <i class="fas fa-user"></i>
            </div>
            <div>
               <i class="fas fa-question"></i>
               <i class="fas fa-arrow"></i>
            </div>
         </div>
      </div>
   </div>
</template>

<script>
export default {};
</script>

<style>
.accueil {
  display: flex;
  align-items: center;
}
.accueil > p {
  color: white;
  font-size: 14px;
  margin: 0px;
  padding-left: 15px;
  padding-right: 15px;
  border-right: 1px #375188 solid;
}
.id {
  display: flex;
  flex-direction: row;
  align-items: center;
  color: white;
}
.id > img {
  margin-right: 5px;
}
.id > p {
  margin: 0px;
  font-size: 14px;
  padding-right: 15px;
  border-right: 1px #375188 solid;
}
.guy {
  height: 30px;
  border-radius: 50%;
}
.navbar {
  background: #4564a7;
  border-bottom: 1px rgb(39, 39, 39) solid;
}
.navbar > .container > div > .fa-facebook {
  color: white;
}

.navbar > .container {
  width: 80%;
}

.navbar > .container > div > .search-input {
  height: 30px;
  border-right: 0px;
}

.container > div {
  display: flex;
  align-items: center;
}

.search-navbar.input-group-text {
  border-top-right-radius: 5% !important;
  border-bottom-right-radius: 5% !important;
  border-left: 0px;
  height: "100px";
  width: 60px;
  display: flex;
  justify-content: center;
}

.container > div {
  display: flex;
  flex-direction: row;
}
</style>