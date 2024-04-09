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
}

.primary {
	background-color: #8d2eff;
	border: 2px solid #6829b3;
}

.secondary {
	background: linear-gradient(to right, #ffcc33, #ffb347);
}
</style>
