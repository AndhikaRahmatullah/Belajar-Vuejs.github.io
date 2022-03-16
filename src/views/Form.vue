<template>
	<div class=""></div>
	<div class="">
		<div class="">
			<dataInput labelName="Masukan Disini :" />
		</div>
	</div>
</template>

<script>
	import Tombol from "@/components/Tombol.vue";
	import dataInput from "@/components/dataInput.vue";

	export default {
		name: `form`,
		data() {
			return {};
		},
		components: { Tombol, dataInput },
	};
</script>
