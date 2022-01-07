<template>
  <h1>{{title}}</h1>
  <Modal header="" />
  <input type="text" ref="name">
  <button @click="handleClick">click me</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {Modal},
  data(){
    return{
      title: 'my first Vue'
    }
  },
    methods: {
      handleClick() {
        console.log(this.$refs.name)
        this.$refs.name.classList.add('actice')
        this.$refs.name.focus()
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
