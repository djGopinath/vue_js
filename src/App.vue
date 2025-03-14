<template>  
//Accessing Methods
<h2>Add Mehtod - {{add(2,4,4)}}</h2>
<h3>Multiply Method {{multiply(baseValue)}}</h3>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      baseMultiplier:5,
      baseValue:1,
    };
  },
  //method creation
  methods:{
    add(a,b,c){
      return a+b+c;
    },
    multiply(num){
     return num*this.baseMultiplier*this.baseValue;
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
