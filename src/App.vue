<template>
  <div>
	<h1>Witaj w systemie zapisów na zajęcia</h1>
	<div v-if="!loggedIn">
		<label>Zaloguj się emailem</label>
		<input type="text" v-model="email">
		<button @click="logMeIn()">Zaloguj się</button>
	</div>
	
	<div v-else>
		<h2>Witaj {{email}}</h2>
		<a @click="logOut()">Wyloguj</a>
	</div>
  </div>
</template>

<script>
import "milligram";
export default {
	data() {
		return {
			email: '',
			loggedIn: false,
		};
	},
	
	methods: {
		logMeIn() {
			this.loggedIn = true;
		},
		
		logOut() {
			this.loggedIn = false;
			this.email = '';
		}
		
	}

  }
</script>

<style>

</style>
