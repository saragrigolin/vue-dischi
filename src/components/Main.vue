<template>
  <div class="container-70 my-5">
		<div class="row row-cols-5">
			<div class="col">
				<div class="spotify-card">
					<img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<h2>new jersy</h2>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
// import axios from 'axios';

export default {
  name: "Main",
}
</script>


<style lang="scss">
@import "../assets/scss/style.scss";
.container-70 {
	width: 70%;
	margin: auto;
	.spotify-card {
		background-color: $headerBackground;
		display: flex;
		flex-direction: column;
		align-items: center;
		img {
			width: 100%;
		}
		h2 {
			text-transform: uppercase;
		}
	}
}
</style>