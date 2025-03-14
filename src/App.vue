<template>

<!-- shorthand property of v-bind is : with attributes  'v-bind:class' is converted to ':class' -->
<h1 :id="headingId">Heading</h1>
<button :disabled="isDisabled">Submit</button>
<h2 class="underline">Underlined Text</h2>
<h3 class=underline :class="status">Status</h3>
<h4 :class="isPromoted && 'promoted'">Promoted Movies</h4>
<h5 :class="isSoldOut ? 'sold-out':'new-movie'">Soldout? Movies</h5>
<h6 :class="[isPromoted && 'promoted', isSoldOut && 'sold-out']">Array Conditioned class</h6>

<!-- style With condition -->
<h1 :class="{
  promoted:isPromoted,
  new:!isSoldOut,
  'sold-out':isSoldOut
}">object Conditioned Class</h1>

<!-- inline Style -->
<h2 :style="{
  color:highlightendColor,fontSize:highlightendFont
}">Inline Style</h2>

<!-- Style object -->
<h3 :style="highlightendStyle">StyleObject</h3>

<!-- Style object with Array -->
<h4 :style="[succesStyleObject,dangerStyleObject,baseStyleObject]" :class="'promoted'">Style object with Array</h4>
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

     //style Object will pass into array
     baseStyleObject:{
      fontSize:'30px',
      padding:'10px'
     },

     succesStyleObject:{
        color:'pink',
        border:'2px solid #2c3e50',
        backgroundColor:'white',
        padding:'20px'
     },
      dangerStyleObject:{
        color:'red',
        border:'3px solid #990b06',
        backgroundColor:'#f57e7a',
        padding:'20px'
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
