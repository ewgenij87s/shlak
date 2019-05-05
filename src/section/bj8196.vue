<template lang="pug">
	div.section
		h3.title
			| Женские брюки  
			span
				| Adidas 7/8 Sailor Pant (small)
			p
				| Укороченный фасон 
		.section__img
			img.foto(
				class="image"
				v-for="(image,i) in images" 
				:src="require('../assets/' + image)" 
				@click="index = i"
				)
			vue-gallery-slideshow(
				:images="images" 
				:index="index" 
				@close="index = null")
</template>

<script>
import VueGallerySlideshow from "../components/GallerySlideshow.vue";
import sectionStyle from "../components/sectionStyle.sass";
export default {
	name: "bj8196",
	data: function() {
		return {
			images: [
				'bj8196/1.jpg',				
				'bj8196/2.jpg',				
				'bj8196/3.jpg',				
				'bj8196/4.jpg',				
				'bj8196/5.jpg',				
				'bj8196/6.jpg',				
				],
				index: null
		}
	},
	components: {
		VueGallerySlideshow
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">

</style>
