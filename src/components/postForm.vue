<template>

<div class="add-post">
    <form>
      <h4>Add post</h4>
      <input type="text" placeholder="post title" v-model="post.title" @input="title = $event.target.value">
      <input type="text" placeholder="post text" v-model="post.text" @input="text = $event.target.value">
      <button class="addPost" type="submit" @click="createPost">Confirm</button>
    </form>
</div>

</template>


<script>
export default{
    data(){
        return {
            post: {
                title: '',
                text: ''
            }
        }
    },
    methods: {
    createPost(){
        this.$emit('create', this.post)
        event.preventDefault();
        this.post = {
            title: '',
            text: ''
        }
      
    },

    create(){

    }
}
}

</script>


<style scoped>
input{
  width: 100%;
  padding: 15px;
  border: 1px solid green;
  margin: 10px 0;
}

.add-post{
  margin-bottom: 50px;
  width: 100%;
}

form{
  display: flex;
  flex-direction: column;
}

button{
  /* height: 30px; */
  width: 100px;
  margin: 10px 0;
  padding: 10px;
  text-align: center;
  align-self: flex-end;
  border: 1px solid green;
}
</style>