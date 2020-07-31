<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <NewComponent/>
    <ul>
      <li v-bind:key="pkm.id" v-for="pkm in pokemon">{{pkm.name + pkm.level}}</li>
    </ul>
    <HelloWorld msg="Welcome to Your Vue App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import NewComponent from './components/NewComponent.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    NewComponent,
  },

  data(){
    return{
      pokemon: [
        {
          id: 1,
          name: "Charizard",
          level: 55
        },
        {
          id: 2,
          name: "Venusaur",
          level: 66
        }
      ]
    }

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
