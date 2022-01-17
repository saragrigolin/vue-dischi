<template>
	<header>
		<div class="container-fluid">
			<img class="py-2" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="">
		</div>
	</header>
</template>

<script>
export default {
	name: "Header",
}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";
header {
    background-color: $headerBackground;
		img {
			height: 55px;
		}
  }


</style>