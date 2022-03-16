<template>
	<div class="mx-10">
		<p>Tambah tugasmu disini :</p>
		<input type="text" v-model="newTask" class="border-2 outline-none focus:border-purple-600 px-2 focus:scale-110 hover:border-purple-300 transition-all" />
		<button class="bg-gray-600 text-white p-1 mx-3 rounded-lg hover:bg-red-600 hover:scale-95 transition-all" @click.prevent="addTask()">Tambah</button>
		<ul class="mt-2">
			<li v-for="(item, index) in task" :key="item">
				<i v-if="item.done">Daftar :</i>
				<b v-else>{{ index }} - {{ item.daftar }}</b>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: `List`,
		data() {
			return {
				newTask: "Makan ikan asin",
				task: [{ done: true, daftar: " " }],
			};
		},
		methods: {
			addTask() {
				alert(`kamu menambahkan : ${this.newTask}`);
				this.task.push({ daftar: this.newTask });
				this.newTask = " ";
			},
		},
	};
</script>
