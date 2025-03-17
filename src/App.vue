<template>  
  <h3>Full Name is {{fullname}}</h3>
  <button @click="items.push({id:4,
        name:'Item 4',
        price:400})">Total</button>
  <h4>Total Amount is {{total}}</h4>
 <template  v-for="item in items" :key="item.id">
  <h2 v-if="item.price>200">{{item.name}}</h2>
 </template>
 <h4 v-for="it in expensiveItem" :key="it.id">{{it.name}}</h4>
</template>

<script>  

export default {
  name: 'App',
  data(){
    return{
      firstName:'John',
      lastName:'Doe',
      items:[{
        id:1,
        name:'Item 1',
        price:100
      },
      {
        id:2,
        name:'Item 2',
        price:200
      },
      {
        id:3,
        name:'Item 3',
        price:300
      }]
    };
  },
  methods:{},
  computed:{
  fullname(){
    return `${this.firstName}-${this.lastName}`;
  },
  total(){
    return this.items.reduce((total,curr)=>(total=total+curr.price),0)
  },
  expensiveItem(){
    return this.items.filter((item)=>item.price > 100)
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
