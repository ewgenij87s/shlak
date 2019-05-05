<template lang="pug">
	div.section
		h3.title
			| Футболка женская тенисная 
			span
				| Adidas climalite (small)
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
	name: "aj3218",
	data: function() {
		return {
			// ПИЗДЕЦ №1 - не работают адреса картинок из папки assets. Адреса через https срабатывают
			images: [
				'aj3218/1.jpg',				
				'aj3218/2.jpg',				
				'aj3218/3.jpg',				
				'aj3218/4.jpg',				
				'aj3218/5.jpg',				
				'aj3218/6.jpg',				
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
