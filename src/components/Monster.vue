<template>
<div><h4>Monster Name: {{monster.name}}</h4>
  <p>Health:{{monster.health}}</p>
  <p>Attack{{monster.attack}}</p>
  </div>
  
</template>
<script>
export default {
 props: ['monster']
}
    
</script>
<style>

</style>
