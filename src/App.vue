<template>
	<div id="app">
		<TheHeader />
		<AppShowcase />
		<AppServices />
		<AppAbout />
		<AppSuccess />
		<AppTestimonials />
		<AppBlog />
		<AppContact />
		<TheFooter />
	</div>
</template>

<script>
import TheHeader from "@/components/layout/TheHeader";
import TheFooter from "@/components/layout/TheFooter";

import AppShowcase from "@/components/landing/AppShowcase";
import AppServices from "@/components/landing/AppServices";
import AppAbout from "@/components/landing/AppAbout";
import AppSuccess from "@/components/landing/AppSuccess";
import AppTestimonials from "@/components/landing/AppTestimonials";
import AppBlog from "@/components/landing/AppBlog";
import AppContact from "@/components/landing/AppContact";
export default {
	name: "App",
	components: {
		TheHeader,
		TheFooter,
		AppShowcase,
		AppServices,
		AppAbout,
		AppSuccess,
		AppTestimonials,
		AppBlog,
		AppContact,
	},
};
</script>

<style lang="scss">
@import "@/assets/sass/app.scss";
</style>
