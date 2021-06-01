<template>
  <div class="home">
    <div class="search-box">
         <i class="fas fa-search"></i><input type="text" class="search">
    </div>
    <HelloWorld msg="Météo Du Monde"/>
    <div class="info">Utilisez la barre de recherche pour connaitre <br> le temps qu'il fait dans votre ville</div>
    <div class="date">Lundi 01/06/2021</div>
    <div class="ville">Bruxelles, Belgium</div>
    <div class="meteo">
      <div class="temperature">24°c</div>
      <div class="temps">Soleil</div>
    </div>
    
    
    
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style>
  .hello {
    width: 320px;
    margin: 20px auto;
    align-self: center;
    color: rgb(62, 136, 20);
    border: 1px solid rgb(62, 136, 20);
  }
  .info {
    font-size: 18px;
    font-weight: bold;
    color: rgb(47, 95, 19);
  }
  .date {
    margin-top: 22px;
    font-weight: bold;
    color: rgb(39, 68, 22);
  }
  .ville {
    margin: auto;
    width: 280px;
    height: 50px;
    border-radius: 15px 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    background-color: rgba(255, 255, 255, 0.2);
    color: rgb(13, 241, 192);
    font-family: 'Times New Roman', Times, serif;
    font-weight: bold;
    box-shadow: 2px 3px rgba(0, 0, 0, 0.1);
  }
  .meteo {
    margin: 20px auto;
    width: 250px;
    height: 200px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    background-color: rgba(255, 255, 255, 0.3);
    border-radius: 20px;
    box-shadow: 3px 6px rgba(0, 0, 0, 0.1);
  }
  .temperature {
    font-size: 95px;
    font-weight: 800;
    color: whitesmoke;
  }
  .temps {
    font-size: 30px;
    font-weight: 700;
    color: rgb(200, 252, 247);
  }
  .search-box {
    position: relative;
    bottom: 60px;
    right: 100px;
    float: right;
    height: 30px;
    width: 160px;
    background-color: rgba(255, 255, 255, 0.3);
    display: flex;
    align-items: center;
    border-radius: 20px;
  }
.search-box > i {
  margin-left: 10px;
}
.search-box > .search {
  
  height: 30px;
  width: 125px;
  background-color: rgba(255, 255, 255, 0.0);
  border-radius: 20px;
  border: none;
  outline: none;
  padding-left: 10px;

}
  /*.search {
  height: 20px;
  width: 200px;
  background-color: rgba(255,255,255, 0.3);
  font-size: 16px;
}*/
</style>
