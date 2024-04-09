<template>
	<Nav :selected="1">
		<h1 class="title">Himmelblå Børnehave</h1>
		<p class="description">
			Velkommen til Himmelblå Børnehave! <br />
			Vi skaber et kærligt og inkluderende miljø, hvor leg, læring og
			fantasi blomstrer.
		</p>

		<Button type="link" href="/kontakt" styles="primary">Kontakt os</Button>
	</Nav>

	<section id="calendar">
		<CalendarCard
			day="10"
			month="December"
			title="Tur i sandkassen"
			description="Tag dine børn en tur sandkassen (og måske efterlad dem)"
			time="12:00 - 16:00"
		/>
		<CalendarCard
			day="10"
			month="December"
			title="Tur i sandkassen"
			description="Tag dine børn en tur sandkassen (og måske efterlad dem)"
			time="12:00 - 16:00"
		/>
		<CalendarCard
			day="10"
			month="December"
			title="Tur i sandkassen"
			description="Tag dine børn en tur sandkassen (og måske efterlad dem)"
			time="12:00 - 16:00"
		/>
		<CalendarCard
			day="10"
			month="December"
			title="Tur i sandkassen"
			description="Tag dine børn en tur sandkassen (og måske efterlad dem)"
			time="12:00 - 16:00"
		/>
	</section>

	<Footer></Footer>
</template>

<style scoped>
#calendar {
	padding: 70px 0;

	max-width: 1180px;
	margin: 0 auto;

	display: grid;
	grid-template-columns: 1fr 1fr;
	gap: 20px;
}
</style>

<style>
/* CSS (global) */
</style>
