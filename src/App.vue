<template>
<h1>{{title}}</h1>
<p ref="motto"></p>
<div class="inputform">
  <input type="text" ref="name" />
  <button @click="addClass">Click me</button>
</div>

</template>

<script>

export default {
  name: 'App',

  data(){
  return {
    title: 'Restarting my template :)',
  }
},
methods: { 
  addClass() {
    console.log('clicked');
    this.$refs.name.classList='name'
    this.$refs.name.focus()
    this.$refs.motto.innerHTML="Hapinned as usual"
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
h1{
  color: red;
}

.inputform {
  display: flex;
  justify-content: center;
}

.name {
  background-color: greenyellow;
}
</style>
