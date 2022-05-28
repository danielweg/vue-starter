<template>
  <div>
	<h1>Twój email to {{ email }}</h1>
	<div class="bad" v-if="email.length < 10">Za krotki adres</div>
	<div v-else-if="email.length < 20">OK</div>
	<div class="bad" v-else>Za dlugi adres</div>
	{{email.length}}
	<input type="text" v-on:keyup.enter="alertMyEmail" v-model="email">
	<button @click="alertMyEmail()">Wyswietl email</button>
	
  </div>
</template>

<script>
export default {
	data() {
		return {
			email: '',
		}
	},
	
	methods: {
		alertMyEmail() {
			alert(this.email);
		},
		
	}

  }
</script>

<style>
.bad {
	color: red;
}
</style>
