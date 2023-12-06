<!-- <template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
</style> -->
<template>
  <div class="app">
      <post-form
        @create="createPost"
      />
      <post-list 
       :posts="posts"
      />

  </div>
</template>
<script>
import PostForm from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";
export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'javascript', body: 'Описание поста JS'},
        {id: 2, title: 'python', body: 'Описание поста PY'},
        {id: 3, title: 'php', body: 'Описание поста PHP'},
        {id: 4, title: 'node', body: 'Описание поста Node'},
      ],
    }
  },
  methods: {
    createPost(post){
      this.posts.push(post);
    },
  }
}
</script>
<style>
* {
font-family: sans-serif;
 margin: 0;
 padding: 0;
  box-sizing: border-box;
}

h1{
  padding:20px;
}

.app{
  padding: 20px;
}
</style>




