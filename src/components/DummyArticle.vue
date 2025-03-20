<template>
   <div>
    <h2 v-bind="$attrs">{{ title }}</h2>
    <h2>Likes - {{ likes }}</h2>
    <h2>Published - {{ isPublished ? 'Yes' : 'No' }}</h2>
  </div>
</template>

<script>
    export default {
        name: "DummyArticle",
        props: {
            title:{
                type: String,
                required:true,
                default: "Article Title",
            },
            likes: Number,
            isPublished: Boolean,
        },
        inheritAttrs: true, 
    }
</script>

<style scoped>

</style>