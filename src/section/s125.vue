<template lang="pug">
	div.section
		h3.title
			| Шорты женские велосипедные (small)
			br
			span
				| Funkier Ridesse 8 Panel Ladies Cycling Shorts
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
	name: "s125",
	data: function() {
		return {
			// ПИЗДЕЦ №1 - не работают адреса картинок из папки assets. Адреса через https срабатывают
			images: [
				's125/1.jpg',				
				's125/2.jpg',				
				's125/3.jpg',				
				's125/4.jpg',				
				's125/5.jpg'				
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
