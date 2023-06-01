<template>
     <div class="container">
          
     <table class="table">
  <thead>
    <tr>
      <th scope="col-3">#</th>
      <th scope="col-3">{{title1}}</th>
      <th scope="col-3">{{title2}}</th>
      
    </tr>
  </thead>
  <tbody>
    <tr v-for="(game, index) in games" :key="game.index">
      <th scope="row"> {{index+1}}</th>
      <td>
        {{game}}
      </td>
      <button type="button" @click= "eliminar(index)" class="btn btn-danger">Eliminar</button>
    </tr>
  
  </tbody>
</table>
</div>
</template>

<script>
export default {
    name: 'game-component',
    props: {games: {
        type: Array,
        required: true
    }},
    data: function(){
        return {
      title1 : "Juego",
      title2 : "Eliminar juego de tu lista",}
        
    },
    
    methods: {
        eliminar (index) {
            this.$emit ("delete", index)
        }
    }
    
}
</script>

<style scoped>
    .conntainer {
        margin: 0;
        padding: 0;
        
    }
</style>