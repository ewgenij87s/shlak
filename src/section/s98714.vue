<template lang="pug">
	div.section
		h3.title
			| Футболка мужская (small, на высокого человека) 
			span
				| Adidas ID Stadium Tee 
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
	name: "s98714",
	data: function() {
		return {
			// ПИЗДЕЦ №1 - не работают адреса картинок из папки assets. Адреса через https срабатывают
			images: [
				's98714/1.jpg',				
				's98714/2.jpg',				
				's98714/3.jpg',				
				's98714/4.jpg',				
				's98714/5.jpg',				
				's98714/6.jpg',				
				's98714/7.jpg'			
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
