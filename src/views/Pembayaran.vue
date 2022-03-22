<template>
	<div class="mt-10 ml-5">
		<div>
			<button @click="tes()" class="bg-cyan-400 rounded-lg py-1 px-3 transition-all hover:bg-red-500 hover:scale-90 hover:text-white hover:shadow-lg active:scale-75 active:bg-cyan-400">Lihat</button>
			<p>{{ isi }}</p>
		</div>

		<div class="mt-5">
			<span>Pilih Jenis Kendaraan : </span>
			<input type="text" list="nambar" v-model="inputVal" class="border-2 rounded-lg border-cyan-400 hover:border-red-400 focus:outline-none focus:border-red-600" />
			<datalist id="nambar">
				<option value="Mobil"></option>
				<option value="Motor"></option>
				<option value="Helikopter"></option>
				<option value="Pesawat Jet"></option>
				<option value="Kapal Pesiar"></option>
			</datalist>
			<button class="bg-cyan-400 rounded-lg py-[2px] px-3 ml-3 transition-all hover:bg-red-500 hover:text-white hover:shadow-lg active:scale-75 active:bg-cyan-400" @click="(a = !a), ganti()">{{ keterangan }}</button>
			<div class="mt-10" v-for="item in daftar" :key="item">
				<div class="" v-if="a"></div>
				<div class="" v-else-if="!a">
					<p v-if="inputVal == undefined"></p>
					<p v-else-if="inputVal == item.namaBarang">
						Jenis: {{ item.namaBarang }} <br />
						Harga: {{ item.harga }}
					</p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		name: `pembayaran`,
		data() {
			return {
				isi: ``,
				a: true,
				b: false,
				keterangan: `Tampilkan`,
				inputVal: undefined,
				daftar: [
					{ namaBarang: `Mobil`, harga: 30000 },
					{ namaBarang: `Motor`, harga: 20000 },
					{ namaBarang: `Helikopter`, harga: 50000 },
					{ namaBarang: `Pesawat Jet`, harga: 65000 },
					{ namaBarang: `Kapal Pesiar`, harga: 55000 },
				],
			};
		},
		computed: {},
		methods: {
			tes() {
				const a = this.daftar;
				let aa = ``;
				for (let i = 0; i < a.length; i++) {
					let namaBarang = a[i].namaBarang;
					let harga = a[i].harga;
					aa += "Jenis :  " + namaBarang + "  Harga :  " + harga;
					console.log(aa);
				}
				return (this.isi = aa);
			},
			ganti() {
				if (this.keterangan == `Tampilkan`) {
					return (this.keterangan = `Sembunyikan`);
				} else {
					return (this.keterangan = `Tampilkan`);
				}
				// if (this.keterangan == ``) {
				// 	return (this.keterangan = this.keterangan2);

				// return `aaa`;
			},
		},
	};
</script>
