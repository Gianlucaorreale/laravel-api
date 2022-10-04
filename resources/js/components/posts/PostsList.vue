<template>
   <section id="posts-list">
      <h2>Posts</h2>
      <ul v-if="posts.length">
         <li v-for="post in posts" :key="post.id">
            {{post.title}}
        </li>
      </ul>
      <h5 v-else>nessun post</h5>
   </section>
</template>

<script>
import Axios from 'axios';

  export default{
     name:'PostsList',
     data(){
        return {posts: []};
     },
     methods:{
       fetchPosts(){
          Axios.get('http://localhost:8000/api/posts')
          .then(res=>{
            this.posts = res.data;
          });
       },
     },
     mounted(){
        this.fetchPosts();
     }
      
     
  };
</script>

