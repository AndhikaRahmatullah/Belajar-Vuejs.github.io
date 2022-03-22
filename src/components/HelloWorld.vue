<template>
	<div class="text-center">
		<p>
			Nama <span>{{ nama }}</span>
		</p>
		<p>
			Umur <span>{{ umur }}</span>
		</p>
		<p>
			Semester <span>{{ semester }}</span>
		</p>
		<!-- Mengirim data dari child(HelloWord) ke parent(HomeView) -->
		<button @click="changeSemester" class="bg-cyan-500 p-2 rounded-lg mt-3">Ubah Semester</button>
	</div>
</template>

<script>
	export default {
		name: `HelloWorld`,
		// props berisi array
		// Mengirim data dari parent(HomeView) ke child(HeloWord)
		props: [`nama`, `umur`, `semester`],
		data() {
			return {
				newSemester: `Lulus !`,
			};
		},
		methods: {
			// methods berisi function
			// Mengirim data dari child(HelloWord) ke parent(HomeView)
			changeSemester() {
				// jika event di click akan menghasilkan data newSemester
				this.$emit("changeSemester", this.newSemester);
			},
		},
	};
</script>
