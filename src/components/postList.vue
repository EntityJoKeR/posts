<template>
<div class="post" v-for="post in posts" :key="post.id">
    <div class="post-name"><strong>Name: {{ post.title }}</strong></div>
    <div class="post-text"><strong>Description: {{ post.text }}</strong></div>
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

<style>
.post{
  border: 2px solid green;
  padding: 15px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  flex-wrap: nowrap;
  margin: 10px auto;
}
</style>