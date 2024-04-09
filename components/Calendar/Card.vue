<script setup>
const props = defineProps({
	day: String,
	month: String,
	time: String,
	title: String,
	description: String,
	even: Boolean,
})
</script>

<template>
	<article :class="{ even: props.even }">
		<div class="date">
			<h2 id="day">{{ props.day }}</h2>
			<p id="month">{{ props.month }}</p>
		</div>
		<div class="information">
			<h3 id="title">{{ props.title }}</h3>
			<p id="time">{{ props.time }}</p>
			<p id="desc">{{ props.description }}</p>
		</div>
	</article>
</template>

<style scoped>
#day {
	font-size: 8rem;
	line-height: 8rem;
}

#month {
	font-size: 1.8rem;
}

#title {
	font-size: 2.4rem;
}

#time {
	font-size: 1.6rem;
	margin-top: 9px;
}

#desc {
	font-size: 1.7rem;
	margin-top: 20px;
}

article {
	border: 6px solid #ffb347;
	border-radius: 10px;

	display: flex;
}

.even {
	border: 6px solid #6829b3;
}

.date {
	min-width: 20%;
	background-color: #f7f6fe;
	border-radius: 10px 0 0 10px;

	text-align: center;
	display: flex;
	flex-direction: column;
	gap: 15px;

	padding: 32px;
}

.information {
	padding: 32px;

	display: flex;
	flex-direction: column;
}
</style>
