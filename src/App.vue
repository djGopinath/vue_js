<template>
<h1 v-bind:id="headingId">Heading</h1>
<button v-bind:disabled="isDisabled">Submit</button>
<h2 class="underline">Underlined Text</h2>
<h3 class=underline v-bind:class="status">Status</h3>
<h4 v-bind:class="isPromoted && 'promoted'">Promoted Movies</h4>
<h5 v-bind:class="isSoldOut ? 'sold-out':'new-movie'">Soldout? Movies</h5>
<h6 v-bind:class="[isPromoted && 'promoted', isSoldOut && 'sold-out']">Array Conditioned class</h6>
<h1 v-bind:class="{
  promoted:isPromoted,
  new:!isSoldOut,
  'sold-out':isSoldOut
}">object Conditioned Class</h1>
<h2 v-bind:style="{
  color:highlightendColor,fontSize:highlightendFont
}">Inline Style</h2>
<h3 v-bind:style="highlightendStyle">StyleObject</h3>


</template>

<script>

export default {
  name: 'App',
  data(){
    return{
     headingId:'header',
     isDisabled:false,
     status:'danger',
     isPromoted:true,
     isSoldOut:true,
     highlightendColor:'orange',
     highlightendFont:'20px',
     highlightendStyle:{
      color:'purple',
      fontSize:'10px',
      margin:'60px'
     },
     baseStyleObject:{
      fontSize:'30px',
      padding:'10px'
     },
     succesStyleObject:{
        color:'pink',
        border:'2px solid #2c3e50',
        backgroundColor:'white'

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
