<template>
  <div class="home">
    <div class="search-box">
         <i class="fas fa-search"></i><input type="text" class="search">
    </div>
    <h1>this the home page</h1>
    
    
    <HelloWorld msg="Welcome to Your Vue.js App"/>
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
