<template>
  <div id="app">
<h1>Monster Smash</h1>
<!-- this button will show the create new monster form -->
<button  @click='showCreate(false)'>Create</button>
<!-- this button show the monsters component-->
<button @click='showAllMonsters(false)'>Show Monsters</button>  


<section v-show="!showMonsters"> <h4>All Monsters:</h4>
  <!-- this div will show a list of all the monsters -->
  <monsters :monsters = 'monsters'></monsters></section>
    
<create v-show="!showCreateForm" :monsters='monsters'></create>

  </div>
</template>

<script>
import Monsters from './components/Monsters';
import Create from './components/Create';
export default {
  name: 'app',
  data () {
    return {
      showCreateForm: true,
     showMonsters: true,
     monsters: [{name: 'jay-z', health: 'at least 5', attack: 'hes got 99 problems, but attack aint one'}]
    
    }
  },
  methods: {
    showCreate(bool){
      this.showCreateForm = bool
  },
  showAllMonsters(bool){
    this.showMonsters = bool
  }

},
  components: {
    monsters: Monsters,
    create: Create
  }
}
</script>

<style>

</style>
