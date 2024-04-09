<template>
	<Nav :selected="4"></Nav>

	<div class="kontakt form">
		<form action="#" method="post"></form>
	</div>

	<div class="form-group">
		<input type="text" id="name" name="name" placeholder="Navn" required />
	</div>
	<input type="tel" id="phone" name="name" placeholder="Telefon" required />

	<div class="form-group">
		<textarea
			id="messager"
			Name="messager"
			placeholder="Besked"
			rows="4"
			required
		></textarea>
	</div>

	<div class="from-group">
		<button type="submit">submit</button>
	</div>
</template>

<style scoped></style>
