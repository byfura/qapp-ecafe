<template>
  <q-page class="justify-center">
  	<div class="row inline q-pa-sm gutter-xs items-stretch">
			<div class="col-6" v-for="post in blogPosts">
				<BlogPost :post="post"></BlogPost>
			</div>
		</div>
  </q-page>
</template>

<style>
</style>

<script>

import axios from 'axios';
import BlogPost from '../components/BlogPost'

export default {
  name: 'PageIndex',
  components: {
  	BlogPost
  },
  data() {
     return {
     	blogPosts: [],
     	loading: false
     }
  },
  methods: {
  	getBlogPosts: function() {
  		this.loading = true;
  		axios.get("http://localhost:8000/api/blog")
  		.then((response) => {
  			this.loading = false;
  			this.blogPosts = response.data;
  			console.log(this.blogPosts);
  		}, (error) => {
  			this.loading = false;
  		})
  	}
  },
  created() {
  	console.log('create');
  	this.getBlogPosts();
  }
}

</script>