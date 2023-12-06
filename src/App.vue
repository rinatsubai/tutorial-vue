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
    <form>
      <h1> Create </h1> <br/>
      <input type="text" class="input" placeholder="title"/> <br/> <br/>
      <input type="text" class="input" placeholder="description"/> <br/> <br/>
      <button class="btn" @click="createPost">Add</button>
    </form>
    <div class="post" v-for="post in posts" v-bind:key="post">
      <div><strong>Title: </strong> {{ post.title }}</div>
      <div><strong>Content: </strong> {{ post.body }}</div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      posts: [
        {id: 1, title: 'javascript', body: 'Описание поста JS'},
        {id: 2, title: 'python', body: 'Описание поста PY'},
        {id: 3, title: 'php', body: 'Описание поста PHP'},
        {id: 4, title: 'node', body: 'Описание поста Node'},
      ]
    }
  },
  methods: {
    createPost
  }
}
</script>
<style>
* {
 margin: 0;
 padding: 0;
  box-sizing: border-box;
}

.app{
  padding: 20px;
}

.post {
  margin: 20px;
  padding: 15px;
  border: 2px solid #eeeeee;
}

.input {
  width: 600px;
  border: 2px solid #eeeeee;
  padding: 15px;
  margin-left: 20px;
  margin-top: 10px;
}

.btn {
  background-color: #eeeeee;
  border: 0px;
  padding: 15px;
  margin-left: 20px;
  width: 600px;
}

form {
  display: flex;
  flex-direction: column;

}
</style>




