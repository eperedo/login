<template>
	<div class="login-image">
		<picture>
			<source v-bind:srcset="doorWebp" type="image/webp">
			<img v-bind:src="door" alt="login image" width="330" height="337" />
		</picture>
	</div>
</template>

<script>

// import door from './../assets/door.png';
// import doorWebp from './../assets/door.webp';

function created() {
	const doorPath = '/static/img/door';
	const pngExt = '.png';
	const webpExt = '.webp';
	this.door = `${doorPath}${pngExt}`;
	this.doorWebp = `${doorPath}${webpExt}`;
}

function data() {
	return {
		door: '',
		doorWebp: '',
	};
}

export default {
	name: 'login-image',
	created,
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

