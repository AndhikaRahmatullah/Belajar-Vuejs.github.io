<template>
	<div class="text-center">
		<img
			alt="Vue logo"
			src="../assets/doraemon.png"
			class="mx-auto w-44"
		/>
	</div>
	<div class="">
		<!-- mengirim data nama dan umur dari parent(HomeView) ke child(HelloWord) -->
		<!-- bind data semester -->
		<HelloWorld
			nama="Andhika"
			umur="20"
			@changeSemester="changeSemester"
			:semester="semester"
		/>
		<Conditional class="mt-2" />
	</div>
</template>

<script>
	// import file child
	import HelloWorld from "@/components/HelloWorld.vue";
	import Conditional from "@/components/Conditional.vue";

	export default {
		name: "HomeView",
		data() {
			return {
				// bind data semester
				semester: `6 (enam)`,
			};
		},
		components: {
			// panggil nama component
			HelloWorld,
			Conditional,
		},
		methods: {
			// setiap ada event pasti ada methods;
			// methods berisi function dan beri parameter untuk aski
			changeSemester(newSemester) {
				// jika di klik ubah this.semester menjadi newSemester
				this.semester = newSemester;
			},
		},
	};
</script>
