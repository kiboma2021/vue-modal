<template>
<h1>{{title}}</h1>
<p ref="motto"></p>
<div class="inputform">
  <input type="text" ref="name" />
  <button @click="addClass">Click me</button>
</div><br><br>

<button type="button" @click.shift="toggleModal" >Open Modal(shift)</button>

<div v-if="showModal" >
  <Modal class="myModal" @close="toggleModal" theme="theme">
    <div class="m-head">
      <h1>{{header}}</h1>
      <span>X</span>
    </div>
    <input type="char">
    
    <p>{{subheader}}</p> <br><br>
    <button>Close Modal</button>
  </Modal>
</div>
</template>

<script>

import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {Modal},
  data(){
  return {
    title: 'Restarting my template :)',
    showModal: false,
    header: 'Modal heading',
    subheader: 'Modal subheading',
    theme: 'machakos',
  }
},
methods: { 
  addClass() {
    console.log('clicked');
    this.$refs.name.classList='name'
    this.$refs.name.focus()
    this.$refs.motto.innerHTML="Hapinned as usual"
  },
  toggleModal(){
    console.log('clicked');
    this.showModal = !this.showModal
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

.m-head {
  display: flex;
  justify-content: space-between;
}
</style>
