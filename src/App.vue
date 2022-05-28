<template>
  <div>
	<h1>Twój email to {{ email }}</h1>
	
	<h2>Twój email to {{ email }}</h2>
	
	{{email.length}}
	<input type="text" v-model="email">
	
  </div>
</template>

<script>
export default {
	data() {
		return {
			email: '',
		};
	}

  }
</script>

<style>

</style>
