<template>
	<div class="mb-10">
		<i>Custom Emit</i> <br />
		Fungsinya untuk mengirim perubahan data dari komponen anak ke komponen induk.<br /><br />
		<i>Props</i> <br />
		Teknik ini berfungsi untuk mengirim data dari komponen induk ke komponen anak.
	</div>
	<div>
		<!-- data text dibawah berada di komponen induk-->
		<h1>{{ text }}</h1>
		<button @click="ubahText" class="bg-red-500 p-2">Ubah text</button>
	</div>
</template>
<script>
	export default {
		name: `customMethodEmit`,
		data() {
			return {
				textBaru: `Text sudah diubah 😪`,
			};
		},
		props: [`text`],
		methods: {
			// buat custom method untuk mengirim perubahan ke komponen induk
			ubahText() {
				// ubahText adalah nama eventnya
				// this.textBaru adalah data di komponen anak dan yang akan menjadi parameter di fungsi/method komponen induknya
				this.$emit(`ubahText`, this.textBaru);
			},
		},
		// daftarkan emits jika menggunakan $emit
		emits: [`ubahText`],
	};
</script>
