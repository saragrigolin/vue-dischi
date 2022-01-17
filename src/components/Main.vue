<template>
  <div class="container-60 my-5">
		<div class="row row-cols-5">
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
				</div>
			</div>
			<div class="col">
				<div class="spotify-card">
					<img class="p-3" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
					<span class="title">new jersy</span>
					<span class="subtitle">Bon Jovi</span>
					<span class="year">1988</span>
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
.container-60 {
	width: 60%;
	margin: auto;
	.col {
		padding: 0.5em 1em;
	}
	.spotify-card {
		background-color: $headerBackground;
		display: flex;
		flex-direction: column;
		align-items: center;
		img {
			width: 100%;
		}
		.title {
			text-transform: uppercase;
			color: white;
			font-weight: 500;
		}
		.subtitle, .year {
			color: $spanColor;
		}
	}
}
</style>