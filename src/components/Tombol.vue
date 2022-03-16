<template>
	<div>
		<button
			class="px-3 py-1 bg-gradient-to-r from-cyan-400 to-cyan-300 m-2 rounded-lg transition-all ring ring-cyan-600 hover:scale-95 hover:shadow-xl hover:shadow-gray-400 hover:text-white hover:ring-cyan-500 active:scale-75 active:text-black"
		>
			{{ textTombol }}
		</button>
	</div>
</template>

<script>
	export default {
		name: "Tombol",
		data() {
			return {};
		},
		props: [`textTombol`],
	};
</script>
