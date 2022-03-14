<template>
	<div class="about">
		<List />
		<Footer />
	</div>
</template>

<script>
	import Footer from "../components/Footer.vue";
	import List from "../components/List.vue";

	export default {
		name: `AboutViwe`,
		data() {
			return {};
		},
		components: {
			Footer,
			List,
		},
	};
</script>
