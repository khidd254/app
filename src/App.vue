<template>
 <h1>{{ title }}</h1>
<div v-if="showModal">
  <Modal theme="" @close="toggleModal">
    <template v-slot:links>
      <a href="#">sign up now!</a>
      <a href="#">more information</a>
    </template>
    <h1>Kennedy Give away</h1>
    <p>Get yourself signals at half price</p>
</Modal>
</div>
<div v-if="showModalTwo">
  <Modal @close="toggleModalTwo">
    <h1>Sign up for classes</h1>
    <p>For newsupdates and classes</p>
</Modal>
</div>
<p>wecome here</p>
<button @click.alt="toggleModal">Open Modal (alt)</button>
<button @click="toggleModalTwo">Open Modal</button>
</template>

<script>
import Modal from './components/Modal.vue' 

export default {
  name: 'app',
  components:{Modal},
  data(){
    return{
      title:'My First Vue App',
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
    },
    toggleModalTwo(){
      this.showModalTwo = !this.showModalTwo
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
