<template>
  <q-card inline>
    <q-card-media>
      <img :src="`assets/blog/` + post.imgsrc" style="float:left;height:15vw;object-fit:cover;">
    </q-card-media>
    <q-card-title class="relative-position">
      <div class="q-title">{{post.title}}</div>
      <div slot="subtitle" class="row items-center">
       	{{post.date}} * {{post.author}}
      </div>
    </q-card-title>
    <q-card-main>
      <p class="text-faded">{{post.body}}</p>
    </q-card-main>
    <q-card-separator />
    <q-card-actions>
    	<div class="full-width">
      	<q-btn flat color="primary" class="float-right">Read More</q-btn>
    	</div>
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  name: 'BlogPost',
  props: {
  	post: Object
  }
}
</script>

<style>
</style>
