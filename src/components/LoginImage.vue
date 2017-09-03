<template>
	<div class="login-image">
		<img v-bind:src="door" alt="login image" />
	</div>
</template>

<script>

import door from './../assets/door.png';

function data() {
	return {
		door,
	};
}

export default {
	name: 'login-image',
	data,
};
</script>

<style lang="scss" scoped>
.login-image {
	background-image: radial-gradient(9% 86%, map-get($colors, blue-tragic) 16%, map-get($colors, green-tragic) 81%);

	img {
		margin-left: -22%;
	}
}
</style>

