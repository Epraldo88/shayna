<template>
	<div class="home"></div>
	<HeaderShayna />
	<HeroShayna />
	<WomanShayna />
	<InstaShayna />
	<PartnerShayna />
	<FooterShayna />
	<!-- Hero Section Begin -->
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from "@/components/HeaderShayna.vue";
import HeroShayna from "@/components/HeroShayna.vue";
import WomanShayna from "@/components/WomanShayna.vue";
import InstaShayna from "@/components/InstaShayna.vue";
import PartnerShayna from "@/components/PartnerShayna.vue";
import FooterShayna from "@/components/FooterShayna.vue";

export default {
	name: "HomeView",
	components: {
		HeaderShayna,
		HeroShayna,
		WomanShayna,
		InstaShayna,
		PartnerShayna,
		FooterShayna,
	},
};
</script>
