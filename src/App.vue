<template>  


  <input type="text" v-model="movie"/>
  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />
 <button @click="movieList = movieList.concat(['Wonder Woman'])">
    Add movie
  </button>
</template>

<script>  

export default {
  name: 'App',
  data(){
    return{
      movie:'Batman',
      movieInfo:{
        title:'',
        actor:'',
      },
      movieList:['Batman', 'Iron Man']
    } 
  },
  methods:{},
  computed:{},
  watch:{
    volume(newVolume,oldVolume){
      if(newVolume > oldVolume && newVolume ===16){
        alert("Listening in High Volume")
      }
    }, 

  movie: {
      handler(newValue) {
        console.log(`Calling API with movie name = ${newValue}`)
      },
      immediate: true,
    },
  movieInfo: {
    handler(newValue) {
      console.log(
        `Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`
      )
    },
    deep: true,
  },

  movieList: {
      handler(newValue) {
        console.log(`Updated list ${newValue}`)
      },
      // deep: true,
    },
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
