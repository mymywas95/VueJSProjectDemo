<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button v-on:click="reverseMessage">Reverse Message</button>
    <input v-model="msg">
  </div>
</template>

<script>
  import todo from './ToDo.vue';
  export default {
    name: 'HelloWorld',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    methods: {
      reverseMessage: function () {
        this.msg = this.msg.split('').reverse().join('')
      }
    },
    components: {
      'todo': todo
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
