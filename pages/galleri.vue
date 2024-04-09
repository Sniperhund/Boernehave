<script setup>
const modalImage = ref()
const modal = ref()

function click(event) {
	const imageSrc = event.target.src

	modal.value.style.display = "flex"
	modalImage.value.style.backgroundImage = "url('" + imageSrc + "')"
}

function close() {
	modal.value.style.display = "none"
}
</script>

<template>
	<Nav :selected="5">
		<h1 class="title">Galleri</h1>
	</Nav>

	<div class="modal" ref="modal">
		<div class="modal-content" ref="modalImage">
			<span class="close" @click="close">&times;</span>
		</div>
	</div>

	<section>
		<div class="column">
			<img src="https://picsum.photos/400/400" @click="click" />
			<img src="https://picsum.photos/400/200" @click="click" />
			<img src="https://picsum.photos/400/300" @click="click" />
			<img src="https://picsum.photos/400/500" @click="click" />
		</div>
		<div class="column">
			<img src="https://picsum.photos/400/600" @click="click" />
			<img src="https://picsum.photos/400/250" @click="click" />
			<img src="https://picsum.photos/400/200" @click="click" />
			<img src="https://picsum.photos/400/250" @click="click" />
		</div>
		<div class="column">
			<img src="https://picsum.photos/400/350" @click="click" />
			<img src="https://picsum.photos/400/250" @click="click" />
			<img src="https://picsum.photos/400/400" @click="click" />
			<img src="https://picsum.photos/400/200" @click="click" />
		</div>
		<div class="column">
			<img src="https://picsum.photos/400/300" @click="click" />
			<img src="https://picsum.photos/400/200" @click="click" />
			<img src="https://picsum.photos/400/300" @click="click" />
			<img src="https://picsum.photos/400/500" @click="click" />
		</div>
	</section>

	<Footer></Footer>
</template>

<style scoped>
.modal {
	display: none;
	position: fixed;
	z-index: 1;
	padding-top: 50px;
	left: 0;
	top: 0;
	width: 100%;
	height: 100%;
	overflow: auto;
	background-color: rgb(0, 0, 0);
	background-color: rgba(0, 0, 0, 0.4);

	justify-content: center;
	align-items: center;
}

.modal-content {
	position: relative;
	min-width: 30%;
	max-width: 70%;
	height: 70%;
	background-repeat: space;
	background-size: contain;
}

.close {
	position: absolute;
	right: 10px;
	top: -13px;
	color: white;
	font-size: 4rem;
	cursor: pointer;
}

section {
	max-width: 1180px;
	margin: 70px auto;

	display: flex;
	flex-wrap: wrap;
	gap: 8px;
}

.column {
	flex: calc(25% - 24px);
	max-width: 25%;
}

.column img {
	width: 100%;
	margin-top: 8px;
	vertical-align: middle;
	width: 100%;
	border-radius: 10px;
	cursor: pointer;
}

@media screen and (max-width: 800px) {
	.column {
		flex: calc(50% - 24px);
		max-width: 50%;
	}
}

@media screen and (max-width: 600px) {
	.column {
		flex: 100%;
		max-width: 100%;
	}
}
</style>
