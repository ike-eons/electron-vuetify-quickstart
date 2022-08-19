<template>
	<div class="login-section">
		<h1>Welcome</h1>

		<v-form>
			<v-container>
				<v-text-field
					v-model="username"
					label="Username"
					outlined
				></v-text-field>
				<v-text-field
					v-model="password"
					label="Password"
					outlined
				></v-text-field>

				<v-btn block elevation="2" large @click="login">Login</v-btn>
			</v-container>
		</v-form>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				username: '',
				password: '',
			};
		},
		methods: {
			login() {
				if (this.username === 'admin' && this.password === 'admin') {
					this.$router.push({ name: 'Home' });
				} else {
					console.log('login credential do no match');
				}
			},
		},
	};
</script>

<style lang="scss">
	.login-section {
		height: 100%;
		min-width: 100%;
		padding: 200px 0;
		flex-direction: column;
		display: flex;
		place-content: center;
		place-items: center;
	}

	.login-btn {
		background-color: #42b983;
		color: white;
	}
</style>
