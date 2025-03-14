<template>
  <h2 v-if="num===0">The Number is Zero</h2>
  <h2 v-else-if="num>0"> The Number is positive</h2>
  <h2 v-else-if="num<0"> The Number is negative</h2>
  <h2 v-else>The Number is not Zero</h2>

  <template v-if="isDisplay">
    <h2>Hello </h2>
    <h2> DEV</h2>
    <h2>Vue</h2>
  </template>

  <h3 v-show="showElement">Using v-show</h3>
   <h3 v-if="showElement">Using v-if</h3>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      num:0,
      isDisplay:true,
      showElement:false
    };
  },
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

.underline{
  text-decoration: underline;
}
.promoted{
  font-style: italic;
}

.new-movie{
  color:green
}

.sold-out{
  color: red;
}
</style>
