<template>
	<div class="login-image">
		<picture>
			<source srcset="/static/img/door.webp" type="image/webp">
			<img src="/static/img/door.png" alt="login image" width="330" height="337" />
		</picture>
	</div>
</template>

<script>

export default {
	name: 'login-image',
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

