<script setup>
const props = defineProps(["type", "href", "styles"])
</script>

<template>
	<a :href="props.href" v-if="props.type === 'link'" :class="props.styles">
		<slot />
	</a>

	<button v-else>
		<slot />
	</button>
</template>

<style scoped>
a,
button {
	padding: 20px 60px;
	color: #fff;
	display: inline-block;
	border-radius: 43.5px;
	font-size: 20px;
	text-decoration: none;
	font-weight: 500;
}

.primary {
	background-color: #8d2eff;
	border: 8px solid #6829b3;
}

.secondary {
	background: linear-gradient(to right, #ffcc33, #ffb347);
	padding: 16px 60px;
	border: 6px solid #ffb347;
	color: #151965;
}
</style>
