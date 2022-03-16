<template>
	<section class="my-5 mx-10">
		<!-- input -->
		<div class="">
			<label for="">
				{{ labelName }}
				<input type="text" v-model="valueBaru" class="border-2 border-cyan-500 rounded-lg transition-all hover:border-cyan-700 focus:scale-110 focus:border-2 focus:border-cyan-500 focus:outline-none px-2" />
			</label>

			<p>Anda Memasukan : {{ valueBaru }}</p>
		</div>

		<!-- data select -->
		<div class="mt-5">
			<!-- data -->
			<div class="">
				<p>Name :</p>
				<ul>
					<li v-for="value in myObject" :key="value" class="list-disc">
						{{ value.title }}
					</li>
				</ul>
			</div>

			<!-- select -->
			<div class="mt-5 flex">
				<label for=""> Pilih Nama Disini : &ensp; </label>
				<select v-model="value" class="border-2 border-gray-400">
					<option v-for="value in myObject" :key="value" :value="[value.title, value.id, value.data]">
						{{ value.title }}
					</option>
				</select>
			</div>

			<!-- output -->
			<div class="mt-2">
				<p v-if="value == undefined || value[1] == null">Data is Undefined</p>

				<p v-else-if="value[2] == null" class="border-2 border-cyan-500 rounded-md p-2">
					id: {{ value[1] }} <br />
					nama: {{ value[0] }} <br />
					data: (Data is Unefined)
				</p>

				<p v-else class="border-2 border-cyan-500 rounded-md p-2">
					id: {{ value[1] }} <br />
					nama: {{ value[0] }} <br />
					data: {{ value[2] }}
				</p>
			</div>
		</div>
	</section>
</template>

<script>
	export default {
		name: `dataInput`,
		data() {
			return {
				value: undefined,
				valueBaru: "",
				a: false,
				myObject: [
					{ id: 1, title: "dika", data: "suka makan orang" },
					{ id: 2, title: "rahmat", data: "suka makan tanah" },
					{ id: 3, title: "dadang", data: "suka sama orang yg ga suka" },
					{ id: 4, title: "mail", data: null },
					{ id: null, title: "kopret", data: null },
				],
			};
		},
		props: [`labelName`],
		methods: {},
	};
</script>
