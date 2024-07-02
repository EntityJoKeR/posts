<template>
  <div>
    <postForm @create="createPost"/>
    <postList :posts="posts" />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import postForm from './components/postForm.vue'
import postList from './components/postList.vue'

export default {
  name: 'App',
  components: {
    postList, postForm
  },

  data() {
    return {
      title: '',
      text: '',

      posts: [
        {id: 1, title: 'title', text: 'text'}
      ],
    
    }
    
  },
  methods: {
    createPost(post){
      this.posts.push(post)
    }
  }
}
</script>







<style>
*{
  box-sizing: border-box;
}




#app{
  padding: 20px;
}
</style>
