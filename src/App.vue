<template>
	<nav class="text-center bg-black text-gray-500 h-10">
		<!-- <router-link to="/"> adalah halaman utama ! -->
		<router-link to="/" class="mx-2 focus:text-white">Home</router-link>
		<router-link to="/about" class="mx-2 focus:text-white"
			>About</router-link
		>
	</nav>
	<router-view />
</template>
