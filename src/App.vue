<template>
	<nav class="text-center bg-black text-gray-500 h-10">
		<!-- <router-link to="/"> adalah halaman utama ! -->
		<router-link to="/" class="mx-2" active-class="text-white">Home</router-link>
		<router-link to="/about" class="mx-2 focus:text-white" active-class="text-white">About</router-link>
		<router-link to="/animation" class="mx-2 focus:text-white" active-class="text-white">Animation</router-link>
		<router-link to="/form" class="mx-2 focus:text-white" active-class="text-white">Formulir</router-link>
		<router-link to="/customMethode" class="mx-2 focus:text-white" active-class="text-white">CustomMethode</router-link>
		<router-link to="/pembayaran" class="mx-2 focus:text-white" active-class="text-white">Pembayaran</router-link>
	</nav>
	<router-view />
</template>
