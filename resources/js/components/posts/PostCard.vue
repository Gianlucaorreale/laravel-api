<template>

<div class="card" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">{{post.title}}</h5>
    <h6 class="card-subtitle mb-2 text-muted"> Post creato il:{{post.created_at}}</h6>
    <p class="card-text">{{post.content}}</p>
   <!-- <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>-->
  </div>
</div>

</template>

<script>
    export default{
       name:'PostCard',
       props: {
        post: Object,
       },
    }
</script>

<style>

</style>