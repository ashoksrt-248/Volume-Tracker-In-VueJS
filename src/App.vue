<template>
  <div id="app">
    <h1> Volume Tracker Application in VueJs</h1>
    <h2 class="volumeHeading">Current Volume:<span> {{ volume }}</span></h2>
    <button @click="volume += 2" class="increase">Increase</button>
    <button @click="volume-= 2" class="decrease">Decrease</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      volume:0
    }
  },
  methods:{},
  computed:{},
  watch:{
    volume(newValue, oldValue){
      if(newValue > oldValue && newValue === 16){
        alert("it is High Volume, Not Recommended")
      }
      if( newValue < oldValue && oldValue === 4){
        alert("it is Low Volume")
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: tan;
  width: 50%;
  margin:0 auto;
  height:200px;
  line-height: 45px;
  
}
.increase{width:100px;background-color: cadetblue;height: 40px;border: 2px solid cadetblue;border-radius: 50%;}
.decrease{width: 100px;background-color: tomato;height: 40px;border:2px solid tomato;border-radius: 50%;}
.volumeHeading{color: steelblue;}
span{color: snow;}
</style>
