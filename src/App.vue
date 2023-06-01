<template>
  <div id="app">
    <nav class="navbar bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand">Tienda Bit-game</a>  
  </div>
</nav>
   
   <tabla :games="games" @delete="eliminar"/> 

    
  </div>
</template>

<script>
import Games from "@/components/Games.vue"

export default {
  name: 'app',
  data () {
    return {
      
      games:["Arena of valor", "Pokemon Unite", "Donkey Kong", "Heroes of the storm", "Valorant", "Genshin Impact"],

    }
  },
  methods: {

    eliminar (index) {
      this.games.splice(index,1)
    }

  },
  components: {
    "tabla":Games
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
  display: inline
}

.container {
  border: solid 1px black;
  padding: 0;
}

.container-fluid {
    
    justify-content: center;
}

nav {
  background-color: gray;
}
</style>
