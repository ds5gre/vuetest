<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <ul>
    <li v-for="hero in dcHeros">
    <h1>{{ hero.name }}</h1>
    </li>
    </ul>
    <input v-model:value="newHero" placeholder="input some text"/>
    <h3>{{ newHero }}</h3>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  
  data(){
    return{
      newHero:"",
      dcHeros: [
        {"name":"Wonder Woman"},
        {"name":"Arrow"},
        {"name":"Super Man"}
      ],
    };
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
}
</style>