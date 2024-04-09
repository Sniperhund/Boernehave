<script setup>
const props = defineProps({
	selected: Number,
})
</script>

<template>
	<div>
		<nav>
			<p id="logo">LOGO</p>

			<a href="/" :class="{ selected: props.selected == 1 }">Hjem</a>
			<a href="/om-os" :class="{ selected: props.selected == 2 }"
				>Om os</a
			>
			<a href="/personalet" :class="{ selected: props.selected == 3 }"
				>Personalet</a
			>
			<a href="/galleri" :class="{ selected: props.selected == 5 }"
				>Galleri</a
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
	min-height: 100vh;
	max-height: 100vh;
	background-color: #ffcc33;
	background-image: url("/header.svg");
	background-position: bottom;
	padding-top: 50px;
}

a {
	text-decoration: none;
	color: #151965;
	padding: 6px 20px;
	border-radius: 18px;
	font-size: 2.2rem;
}

header {
	max-width: 850px;
	text-align: center;
	margin: 0 auto;

	height: 70vh;

	display: flex;
	align-items: center;
	flex-direction: column;
	justify-content: center;
}

img {
	position: absolute;
	bottom: 0;
	/* -moz-user-select: none;
	-webkit-user-select: none;
	user-select: none; */
	width: 100%;
}

.selected {
	border: 3px solid #ffb347;
	background-color: #f7f6fe;
}
</style>
