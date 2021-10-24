<template>
  <div class="app">
    <PostForm @create="createPost" />
    <PostList :posts="posts"/>
  </div>
</template>


<script>
import PostForm from "./components/PostForm";
import PostList from "./components/PostList";
export default {
  components: {PostList, PostForm},
  data(){
    return{
      posts: [
        {
          id: 1,
          title: "Пост о Javascript 1",
          body: "Javascript универсальный язык программирования"
        },
        {
          id: 2,
          title: "Пост о Javascript 2",
          body: "Javascript универсальный язык программирования"
        },
        {
          id: 3,
          title: "Пост о Javascript 3",
          body: "Javascript универсальный язык программирования"
        }
      ]
    }
  },
  methods:{
    createPost(post){
      this.posts.push(post)
    },
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .app{
    padding: 20px;
  }
</style>