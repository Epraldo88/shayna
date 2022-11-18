<template>
	<Carousel
		class="woman-banner spad"
		:items-to-show="3"
		:autoplay="3500"
		:wrap-around="true"
	>
		<Slide v-for="product in products" :key="product">
			<div class="">
				<slide>
					<div class="carousel__item container-fluid">
						<div class="row">
							<div class="col-lg-12 mt-5">
								<div class="product-slider">
									<div class="product-item">
										<div class="pi-pic">
											<img :src="product.ImageSrc" alt="" />
											<ul>
												<li class="w-icon active">
													<a href="#"><i class="icon_bag_alt"></i></a>
												</li>
												<li class="quick-view">
													<router-link to="/product">+ Quick View</router-link>
												</li>
											</ul>
										</div>
										<div class="pi-text">
											<div class="catagory-name">{{ product.Category }}</div>
											<a href="#">
												<h5>{{ product.ItemName }}</h5>
											</a>
											<div class="product-price">
												{{ product.ItemPrice }}
												<span>{{ product.BaitPromo }}</span>
											</div>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</slide>
			</div>
		</Slide>

		<template #addons>
			<Navigation />
		</template>
	</Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Navigation, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
	name: "WomanShayna",
	components: {
		Carousel,
		Slide,
		Navigation,
	},
	data() {
		return {
			products: [
				{
					Category: "Coat",
					ItemName: "Mickey Baggy",
					ItemPrice: "14.00",
					BaitPromo: "35.00",
					// backgroundImg: {
					ImageSrc: "/img/mickey1.jpg",
					// },
				},
				{
					Category: "Sweater",
					ItemName: "Guangzhou Sweater",
					ItemPrice: "$13.00",
					BaitPromo: "",
					// backgroundImg: {
					ImageSrc: "/img/products/women-2.jpg",
					// },
				},
				{
					Category: "Sweater",
					ItemName: "Pure Pineappale",
					ItemPrice: "$34.00",
					BaitPromo: "",
					// backgroundImg: {
					ImageSrc: "/img/products/women-3.jpg",
					// },
				},
				{
					Category: "Bag",
					ItemName: "Slingbag",
					ItemPrice: "$24.00",
					BaitPromo: "",
					// backgroundImg: {
					ImageSrc: "/img/products/women-4.jpg",
					// },
				},
			],
		};
	},
});
</script>

<style scoped></style>
