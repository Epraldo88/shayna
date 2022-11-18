<template>
	<div class="carousel-partner">
		<Carousel
			class="container"
			:items-to-show="5"
			:autoplay="2000"
			:wrap-around="true"
		>
			<Slide v-for="partner in partners" :key="partner">
				<slide>
					<div class="carousel__item">
						<div class="partner-logo">
							<div class="logo-carousel">
								<div class="logo-item">
									<div class="tablecell-inner">
										<img :src="partner.ImageSrc" alt="" />
									</div>
								</div>
							</div>
						</div>
					</div>
				</slide>
			</Slide>
		</Carousel>
	</div>

	<!-- Partner Logo Section End -->
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
	name: "PartnerShayna",
	components: {
		Carousel,
		Slide,
	},
	data() {
		return {
			partners: [
				{
					ImageSrc: "/img/logo-carousel/logo-1.png",
				},
				{
					ImageSrc: "/img/logo-carousel/logo-2.png",
				},
				{
					ImageSrc: "/img/logo-carousel/logo-3.png",
				},
				{
					ImageSrc: "/img/logo-carousel/logo-4.png",
				},
				{
					ImageSrc: "/img/logo-carousel/logo-5.png",
				},
			],
		};
	},
});
</script>

<style scoped>
.carousel-partner {
	background-color: #303030;
}
</style>
