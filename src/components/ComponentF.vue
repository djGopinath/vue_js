<template>
    <div>
<h2>Component F</h2>
<h4>My Name is {{userName}}</h4>
    </div>
</template>

<script>
    export default {
        name:'ComponentF',
        inject:['userName']
    }
</script>

<style scoped>

</style>