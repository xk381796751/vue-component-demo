<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <son :title="title" :text="text" @submit-value="keller"></son>
  </div>
</template>

<script>
  import Son from './Son'
  export default {
    name: 'HelloWorld',
    components: {
      Son
    },
    data() {
      return {
        msg: 'Vue.js',
        title: '标题111',
        text: '正文222'
      }
    },
    methods: {
      keller(val) {
        console.log('val', val)
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
