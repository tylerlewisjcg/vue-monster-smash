<template>

  <form  @submit="addPost">
  <h4>Create New Monster:</h4>
<p>Name:<input v-model="nameInput"/> </p>
<p>Health: <input v-model="healthInput"/></p>
<p>Attack:<input v-model="attackInput"/> </p>
<button  type="submit" >Create</button>
</form>


</template>
<script>
export default {
    data(){
        return {
             nameInput: "",
     healthInput: "",
     attackInput: ""
        }
    },
    methods: {
          addPost(){
      let newMonster = {
        name: this.nameInput,
        health: this.healthInput,
        attack: this.attackInput
        
      }
      this.props.monsters.push(newMonster);
      this.nameInput = '',
      this.healthInput = '',
      this.attackInput = ''
    }
    },
    props: ['monsters']
}
    
</script>
<style>

</style>
