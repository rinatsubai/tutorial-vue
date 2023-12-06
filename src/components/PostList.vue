<template>
    <div>
        <div class="post" v-for="post in posts" v-bind:key="post">
        <div><strong>Title: </strong> {{ post.title }}</div>
        <div><strong>Content: </strong> {{ post.body }}</div>
    </div>
    </div>
</template>

<script>
export default{
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>
.post {
  margin: 20px;
  padding: 15px;
  border: 2px solid #eeeeee;
}
</style>