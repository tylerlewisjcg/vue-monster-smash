<template><div>
  <!-- this button will randomly pick a winning monster -->
  <p>Monster #1: </p>
  <p>Monster #2: </p>
  
<button>Battle!</button>
<monster v-for="(monster, i) in monsters" :key="i" :monster='monster'></monster>
</div>
</template>
<script>
import Monster from './Monster'
export default {
    props: ['monsters']
}
    
</script>
<style>

</style>