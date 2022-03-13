<template>
	<div class="text-center">
		<button @click="toggle" class="bg-cyan-500 rounded-md p-2">
			Toggle
		</button>
		<div class="text-2xl">
			<p v-if="benar" class="text-blue-600">Dika Ganteng</p>
			<p v-else class="text-red-500">Hehehe</p>
		</div>
	</div>
</template>

<script>
	export default {
		name: `Conditional`,
		data() {
			return {
				benar: true,
			};
		},
		methods: {
			toggle() {
				this.benar = !this.benar;
			},
		},
	};
</script>
