<template>  
    <!-- Array string iteration -->
  <h4 v-for="(name,index) in names" :key="name">{{index}}{{name}}</h4>

    <!-- Array of Object iteration -->
  <h5 v-for="(name,index) in fullNames" :key="index">{{name.firstName}} {{name.lastName}}</h5>

    <!-- Array of Array iteration -->
  <div v-for="(actor,index) in actors" :key="index">
    <h2>{{actor.name}}</h2>
    <h4 v-for="(movie,i) in actor.movies" :key="i">{{movie}}</h4>
  </div>

  <!-- object iteration with key and index properties -->
  <h2 v-for="(value,key,index) in myInfo" :key="index">{{index+1}} {{key}} {{value}}</h2>

  <!-- template iteration -->
  <template  v-for="(name,index) in names" :key="name">
  <h4>{{index}}{{name}}</h4>
  <hr/>
  </template>

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
   names:[
    "Steve",
    "Tony Stark",
    "Thanos"
   ],
   fullNames:[{firstName: 'Steve', lastName: 'Robson'}, {firstName: 'Tony', lastName: 'Stark'}, {firstName: 'Thanos', lastName:'Dione'}],
  actors:[
  {
    name: "Diane Keaton",
    movies: ["The Godfather", "Annie Hall"]
  },
  {
    name: "Tony Stark (Robert Downey Jr.)",
    movies: ["Iron Man", "Avengers: Endgame"]
  },
  {
    name: "Clark Kent (Henry Cavill)",
    movies: ["Man of Steel", "Batman v Superman: Dawn of Justice"]
  }
],
myInfo:{
  name:"Dev",
  Designation:"Software Developer",
  Department:"IT"
}
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
