<template>
	<div class="mx-10"><customMethodEmit @ubahText="ubahTextnya" :text="text" /></div>
</template>
<script>
	import customMethodEmit from "@/components/customMethodEmit.vue";
	export default {
		name: `customMethode`,
		data() {
			return {
				text: `Halo dika ganteng`,
			};
		},
		components: {
			customMethodEmit,
		},
		methods: {
			ubahTextnya(textBaru) {
				this.text = textBaru;
			},
		},
	};
</script>
