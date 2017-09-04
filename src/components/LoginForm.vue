<template>
	<div class="login-form">
		<form v-on:submit="signIn">
			<header class="form-header">
				<span class="title">Already Members</span>
				<span class="help">Need help?</span>
			</header>
			<section class="form-content">
				<div class="form-control">
					<label for="email">Email</label>
					<input id="email" type="email" placeholder="Enter your email" v-model="model.email" required>
				</div>
				<div class="form-control">
					<label for="pass">Password</label>
					<input id="pass" type="password" placeholder="Enter your password" v-model="model.password" required>
				</div>
				<div class="form-control">
					<button type="submit" class="btn">Sign In</button>
				</div>
			</section>
		</form>
		<section class="login-options">
			<p>Don't have an account yet</p>
			<a href="#">
				Create an account
			</a>
		</section>
	</div>
</template>

<script>

function data() {
	return {
		model: {
			email: '',
			password: '',
		},
	};
}

function signIn(e) {
	e.preventDefault();
	console.log(`Welcome back ${this.model.email}`);
}

export default {
	name: 'login-form',
	data,
	methods: {
		signIn,
	},
};
</script>

<style lang="scss" scoped>
.login-form {
	align-items: center;
	background-color: map-get($colors, yellow);
	display: flex;
	flex-direction: column;
	justify-content: center;
	width: 100%;

	label {
		display: none;
	}

	form {
		background-color: map-get($colors, white);
		width: 213px;

		.form-header {
			background: map-get($colors, white);
			box-shadow: 0 0 13px 0 map-get($colors, yellow-tragic);
			display: flex;
			justify-content: space-between;
			padding: 17px 11px;

			.title {
				color: map-get($colors, yellow);
				font-size: em(8);
				letter-spacing: 0.89px;
				text-transform: uppercase;
			}

			.help {
				color: map-get($colors, white-tragic);
				font-size: em(9);
				opacity: 0.95;
			}
		}

		.form-content {
			align-items: center;
			display: flex;
			flex-direction: column;
			padding: 17px 11px;

			.form-control {
				margin-bottom: 10px;
				width: 190px;

				input {
					background: #FCFCFD;
					border: 0 solid #ECF0F3;
					border-radius: 3.06px;
					font-size: em(9.4);
					height: 30px;
					width: 100%;
				}

				.btn {
					background: map-get($colors, green-tragic);
					border: none;
					border-radius: 2px;
					color: map-get($colors, white);
					font-size: 10.21px;
					height: 36px;
					width: 100%;
				}
			}
		}
	}

	.login-options {

		text-align: center;

		p {
			color: map-get($colors, white);
			font-size: 11.23px;
			margin-bottom: 0;
			opacity: 0.95;
		}

		a {
			color: map-get($colors, green-tragic);
			font-size: em(11.23);
			opacity: 0.95;
			text-decoration: none;
		}
	}
}
</style>

