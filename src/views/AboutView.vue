<template>
	<div class="about">
		<div class="grid grid-cols-2">
			<List />
			<div class="">
				<input
					type="text"
					class="border border-cyan-500"
					v-model="masuk"
					placeholder="masukan disini"
				/>
				{{ masuk }}
			</div>
			<div class="mx-10 mt-5">
				<p v-for="item in mahasiswa" :key="item">
					Id: {{ item.id }} - Nama: {{ item.nama }} - Semester:
					{{ item.semester }}
				</p>
			</div>
			<div class="grid grid-cols-2 mx-10 mt-5">
				<div class="">
					<p>Id Ganjil :</p>
					<p
						v-for="mahasiswa in mahasiswaganjil"
						:key="mahasiswa"
					>
						Id : {{ mahasiswa.id }} - {{ mahasiswa.nama }}
					</p>
				</div>
				<div class="">
					<p>Id Genap :</p>
					<p
						v-for="mahasiswa in mahasiswagenap"
						:key="mahasiswa"
					>
						Id : {{ mahasiswa.id }} - {{ mahasiswa.nama }}
					</p>
				</div>
			</div>
		</div>
		<Footer />
	</div>
</template>

<script>
	import Footer from "../components/Footer.vue";
	import List from "../components/List.vue";

	export default {
		name: `AboutViwe`,
		data() {
			return {
				masuk: ``,
				mahasiswa: [
					{ id: 1, nama: `Andhika Rahmatullah`, semester: 6 },
					{ id: 2, nama: `Dadang Suparman`, semester: 8 },
					{ id: 3, nama: `Boboboy Angin`, semester: 4 },
					{ id: 4, nama: `Boboboy Air`, semester: 2 },
				],
			};
		},
		computed: {
			mahasiswagenap() {
				return this.mahasiswa.filter(
					(mahasiswa) => mahasiswa.id % 2 === 0
				);
			},
			mahasiswaganjil() {
				return this.mahasiswa.filter(
					(mahasiswa) => mahasiswa.id % 2 === 1
				);
			},
		},
		components: {
			Footer,
			List,
		},
	};
</script>
