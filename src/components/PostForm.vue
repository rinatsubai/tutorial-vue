<template>
    <form @submit.prevent>
      <h1> Create </h1> <br/>
      <input 
        v-model="post.title"
        type="text" 
        class="input" 
        placeholder="title"
      > <br/> <br/>
      <input 
      v-model="post.body"
        type="text" 
        class="input" 
        placeholder="description"
      > <br/> <br/>
      <button 
        class="btn" 
        @click="createPost"
      >
      Add
    </button>
    </form>
</template>

<script>
export default {
        data() {
            return {
                post: {
                    title: '',
                    body: '',
                }
            }
        },
        methods: {
            createPost() {
                this.post.id = Date.now();
                this.$emit('create', this.post, 'second', 'third')
                this.post = {
                    title: '',
                    body: '',
                }
            }
        }
}
</script>

<style scoped>
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