<template lang="pug">
	div.section
		h3.title
			| Джинсы мужские (31W/32L) 
			span
				| CR7 Cristiano Ronaldo 
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
	name: "crd043a",
	data: function() {
		return {
			// ПИЗДЕЦ №1 - не работают адреса картинок из папки assets. Адреса через https срабатывают
			images: [
				'crd043a/1.jpg',				
				'crd043a/2.jpg',				
				'crd043a/3.jpg',				
				'crd043a/4.jpg',				
				'crd043a/5.jpg',				
				'crd043a/6.jpg',				
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
