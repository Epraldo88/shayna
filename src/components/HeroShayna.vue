<template>
	<Carousel class="main-carousel" :autoplay="3500" :wrap-around="true">
		<Slide v-for="content in contents" :key="content">
			<slide>
				<div
					class="carousel__item hero-section set-bg"
					:style="content.backgroundImg"
				>
					<div class="container">
						<div class="row">
							<div class="col-lg-5">
								<span>{{ content.Category }}</span>
								<h1>{{ content.ItemName }}</h1>
								<p>
									{{ content.ItemContent }}
								</p>
								<a href="#" class="primary-btn">Shop Now</a>
							</div>
						</div>
					</div>
				</div>
			</slide>
		</Slide>

		<template #addons>
			<Pagination />
		</template>
	</Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
	name: "HeroShayna",
	components: {
		Carousel,
		Slide,
		Pagination,
	},
	data() {
		return {
			contents: [
				{
					Category: "Bag, Kids",
					ItemName: "Black Friday",
					ItemContent:
						"Lorem ipsum dolor sit amet, consectetur adipisicing elit, seddo eiusmod tempor incididunt ut labore et dolore",
					// BackgroundUrl: "../../public/img/hero-1.jpg",
					backgroundImg: {
						backgroundImage: `url(${require("../../public/img/hero-1.jpg")})`,
					},
				},
				{
					Category: "Baggyyyyy, Kids",
					ItemName: "Black Friday",
					ItemContent:
						"Lorem ipsum dolor sit amet, consectetur adipisicing elit, seddo eiusmod tempor incididunt ut labore et dolore",

					backgroundImg: {
						backgroundImage: `url(${require("../../public/img/hero-2.jpg")})`,
					},
				},
			],
		};
	},
});
</script>

<style scoped>
.carousel__item {
	min-height: 700px;
	width: 100%;
	padding: 0;
	font-size: 20px;
	border-radius: 8px;
	display: flex;
	justify-content: center;
	align-items: center;
}

.carousel__prev,
.carousel__next {
	box-sizing: content-box;
	border: 5px solid white;
}
</style>
