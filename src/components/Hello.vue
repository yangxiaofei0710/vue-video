<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>欢迎来到王者荣耀</h2>
    {{totalPrice}}
    <apple></apple>
    <banana></banana>
  </div>
</template>

<script>
	import Apple from './apple'
	import Banana from './banana'
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
  	Apple,
  	Banana
  },
  computed:{
  	totalPrice () {
  		return this.$store.getters.getTotal
  	}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
