<template>
  <q-page class="justify-center">
  	<div class="row inline q-pa-sm gutter-xs items-stretch">
			<div class="col-6" v-for="post in posts">
				<BlogPost :post="post"></BlogPost>
			</div>
		</div>
  </q-page>
</template>

<style>
</style>

<script>

import BlogPost from '../components/BlogPost'

export default {
  name: 'PageIndex',
  components: {
  	BlogPost
  },
  data() {
     return {
        posts: [
					{
						"id":1,
						"title":"Makin Banyak Kosakata Makin Lancar Bicara Metode sinonim Part 1",
						"date":"2018-09-08",
						"author": "Gede Murta",
						"imgSrc": "blog-1.jpg",
						"body":"Mampu berbicara bahasa inggris dalam kehidupan sehari – hari adalah dambaan masyarakat yang bahasa sehari - harinya bukan bahasa inggris. Hal ini dikarenakan orang yang dapat lancar berbicara bahasa inggris memiliki kesempatan bekerja"
					},
					{
						"id":2,
						"title":"Contoh Percakapan dengan Menggunakan Kata Ensure dalam Bahasa Inggris Beserta Artinya",
						"date":"2018-09-08",
						"author": "Desak",
						"imgSrc": "blog-2.png",
						"body":"Sebelumnya English Cafe Bali telah memberikan perbedaan pengertian antara Assure, Ensure, Insure dan Secure. Masih ada yang ingat tidak dengan perbedaan kata tersebut? Nah, untuk memperjelas lagi pengertian dari kata tersebut, English Cafe"
					},
					{
						"id":3,
						"title":"Contoh Percakapan dengan Menggunakan Kata Ensure dalam Bahasa Inggris Beserta Artinya",
						"date":"2018-09-08",
						"author": "Desak",
						"imgSrc": "blog-2.png",
						"body":"Sebelumnya English Cafe Bali telah memberikan perbedaan pengertian antara Assure, Ensure, Insure dan Secure. Masih ada yang ingat tidak dengan perbedaan kata tersebut? Nah, untuk memperjelas lagi pengertian dari kata tersebut, English Cafe"
					},
					{
						"id":4,
						"title":"Contoh Percakapan dengan Menggunakan Kata Ensure dalam Bahasa Inggris Beserta Artinya",
						"date":"2018-09-08",
						"author": "Desak",
						"imgSrc": "blog-2.png",
						"body":"Sebelumnya English Cafe Bali telah memberikan perbedaan pengertian antara Assure, Ensure, Insure dan Secure. Masih ada yang ingat tidak dengan perbedaan kata tersebut? Nah, untuk memperjelas lagi pengertian dari kata tersebut, English Cafe"
					},
					{
						"id":5,
						"title":"Contoh Percakapan dengan Menggunakan Kata Ensure dalam Bahasa Inggris Beserta Artinya",
						"date":"2018-09-08",
						"author": "Desak",
						"imgSrc": "blog-2.png",
						"body":"Sebelumnya English Cafe Bali telah memberikan perbedaan pengertian antara Assure, Ensure, Insure dan Secure. Masih ada yang ingat tidak dengan perbedaan kata tersebut? Nah, untuk memperjelas lagi pengertian dari kata tersebut, English Cafe"
					},
					{
						"id":6,
						"title":"Contoh Percakapan dengan Menggunakan Kata Ensure dalam Bahasa Inggris Beserta Artinya",
						"date":"2018-09-08",
						"author": "Desak",
						"imgSrc": "blog-2.png",
						"body":"Sebelumnya English Cafe Bali telah memberikan perbedaan pengertian antara Assure, Ensure, Insure dan Secure. Masih ada yang ingat tidak dengan perbedaan kata tersebut? Nah, untuk memperjelas lagi pengertian dari kata tersebut, English Cafe"
					}
		  	]
     };
  }
}

</script>