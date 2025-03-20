<template>  
<ComponentC />
<h4>App component username is  {{name}}</h4>
</template>

<script>  
import ComponentC from './components/ComponentC.vue'
export default {
  name: 'App',
 components:{
  ComponentC
 },
 data(){
  return{
    name:'Delsid'
   }
 },
 provide() {
 return { userName:'Dev'}
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

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}

div{
  width: 300px;
}
</style>
