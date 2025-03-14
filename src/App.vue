<template>  
<h1>Counter - {{count}}</h1>

<h3>{{name}}</h3>

<!-- Add "@" symbol instead of "v-on:" it is shorthand property -->
<button @click="increment">Increament</button>
<button @click="decrement(decrementValue)">Decreament</button>
<button @click="changeName">Change Name</button>

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      name:'DEV',
      decrementValue:2,
      count:0
    };
  },
  //method creation
  methods:{
    changeName(eve){
      this.name='Deva'
      console.log('eve',eve)
    },
    increment(){
        this.count+=1;
    },
       decrement(decValue){
        this.count-=decValue;
    },
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
