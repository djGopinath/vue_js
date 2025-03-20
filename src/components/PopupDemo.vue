<template>
    <div>
<h2>Popup component</h2>
<input type="text" v-model="name"/>
<button @click="$emit('close',name)">Close</button>
    </div>
</template>

<script>
    export default {
        name:'PopupDemo',
        emits:{
            close:(name)=>{
               if(!name){
                return false;
               } else{
                return true;
               }
            }
        },
        data(){
            return{
                name:''
            }
        }
    }
</script>

<style scoped>

</style>