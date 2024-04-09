<script setup>
const props = defineProps({
	selected: Number,
})
</script>

<template>
	<div>
		<nav>
			<p id="logo">LOGO</p>

			<a href="/" :class="{ selected: props.selected == 1 }">Home</a>
			<a href="/om-os" :class="{ selected: props.selected == 2 }"
				>Om os</a
			>
			<a href="/" :class="{ selected: props.selected == 3 }"
				>Personalet</a
			>
			<a href="/kontakt" :class="{ selected: props.selected == 4 }"
				>Kontakt</a
			>
		</nav>
		<header>
			<slot />
		</header>
	</div>
</template>

<style scoped>
nav {
	max-width: 1180px;
	max-height: 100px;
	margin: 0 auto;

	border-radius: 50px;

	background-color: white;

	display: flex;
	align-items: center;

	padding: 16px 50px;
}

#logo {
	margin-right: auto;
}

div {
	background-color: #ffcc33;
	padding-top: 50px;
}

a {
	text-decoration: none;
	color: #151965;
	padding: 6px 20px;
	border-radius: 18px;
	font-size: 2.2rem;
}

.selected {
	border: 1px solid #ffb347;
	background-color: #f7f6fe;
}
</style>
