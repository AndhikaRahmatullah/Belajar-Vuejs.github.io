<template>
	<section class="bg-purple-500 aspect-auto grid grid-cols-3 p-5 mt-5">
		<div class="">
			<img src="../assets/doraemon.png" alt="" class="w-44" />
		</div>
		<div class="my-auto">
			<a :href="ig" target="_blank" class="text-lg px-2"> Instagram</a>
			<a :href="fb" target="_blank" class="text-lg px-2"> Facebook</a>
			<a :href="gh" target="_blank" class="text-lg px-2"> Github</a>
		</div>
		<div class="my-auto">
			<p>{{ jumlah() }}</p>
		</div>
	</section>
</template>

<script>
	export default {
		name: `Footer`,
		data() {
			return {
				ig: `https://www.instagram.com/andhikarhmt_/`,
				fb: `https://www.facebook.com/andhika.rahmatullah.5`,
				gh: `https://github.com/AndhikaRahmatullah`,
			};
		},

		methods: {
			jumlah() {
				let a = new Date();
				return a;
			},
		},
	};
</script>
