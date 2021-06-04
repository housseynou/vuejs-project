<template>
  <div class="home">
    <div class="search-box">
         <i class="fas fa-search"></i><input type="text" class="search" placeholder="une ville..." v-model="query" @keypress="weatherData">
    </div>
    <!--<HelloWorld msg="Météo Du Monde"/> -->
    <h1>Météo Du Monde</h1>
    <div class="info">Utilisez la barre de recherche pour connaitre <br> le temps qu'il fait dans votre ville</div>
    <div v-if="typeof weather.main != 'undefined'">
      <div class="date">{{ dateTime() }}</div>
      <div class="ville">{{ weather.name }}, {{ weather.sys.country }}</div>
      <div class="meteo">
        <div class="temperature"> {{ Math.round(weather.main.temp)}}°c</div>
        <div class="temps">{{ weather.weather[0].description }}</div>
      </div>
    </div>
  </div>
</template>

<!--import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
  
} -->

<script>
// @ is an alias to /src

export default {
  name: 'app',
  data () {
    return {
      api_key: 'bfd8a171586a6251815db6513dd063cd',
      url: 'https://api.openweathermap.org/data/2.5/',
      query: '',
      weather: {},
      lang: 'fr',
      units: 'metric'
    }
  },
  methods: {
      weatherData(e) {
      if (e.key == 'Enter'){
        console.log(this.url);
        fetch(this.url+'weather?q='+this.query+'&units=metric'+'&APPID='+this.api_key+'&lang='+this.lang)
          .then(datas => {
            return datas.json();
        }).then(this.setResults);
        console.log(this.setResults);
      }
    },
    setResults(results){
      this.weather = results;
    }, 
    dateTime(){
                  

            

            //var currentDateWithFormat = new Date().toJSON().slice(0,10).replace(/-/g,'/');

      let d = new Date();
      let y = new Intl.DateTimeFormat('fr', { year: 'numeric' }).format(d);
      let m = new Intl.DateTimeFormat('fr', { month: 'short' }).format(d);
      let da = new Intl.DateTimeFormat('fr', { day: '2-digit' }).format(d);
      return `${da}-${m}-${y}`;   

      //const today = new Date();
      //const date = (today.getDate()+today.getMonth()+today.getFullYear()).toJSON().slice(0,10).replace(/-/g,'/');
      //const time = today.getHours()+':'+today.getMinutes()+':'+today.getSeconds();
      //const datetime = date+' '+time;
      //return datetime;
      //return currentDateWithFormat;
    }
  }
}
</script>

<style>
  h1 {
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
    /*box-shadow: 4px 4px 6px #777;*/
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
    background-color: rgba(255, 255, 255, 0.5);
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
