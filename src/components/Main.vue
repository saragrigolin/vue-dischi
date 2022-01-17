<template>
	<main>
		<div class="container-60 my-5">
			<div v-if="cards" class="row row-cols-5">
				<Card 
				v-for="(card, index) in cards" :key="index" :image="card.poster" :name="card.title" :title="card.title" :artist="card.author" :year="card.year"/>
			</div>
			<div v-else class="loading">
				<h1>Loading...</h1>
			</div>
		</div>
	</main>
</template>

<script>
import axios from 'axios';
import Card from './Card.vue';

    // "response": [
    //     {
    //         "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
    //         "title": "New Jersey",
    //         "author": "Bon Jovi",
    //         "genre": "Rock",
    //         "year": "1988"
    //     },

export default {
  name: "Main",
	components: {
		Card,
	},
	data() {
		return {
			cards: null,
		}
	},
	mounted() {
		setTimeout(() => {
			this.getCards()
		}, 1000);
	},
	methods: {
		getCards() {
			axios.get('https://flynn.boolean.careers/exercises/api/array/music')
			.then((result) => {
				this.cards = result.data.response;
			})
			.catch((error) => {
				console.log(error);
			})
		}
	}
}
</script>


<style lang="scss">
@import "../assets/scss/style.scss";
main {
	.container-60 {
		width: 60%;
		margin: auto;
		.col {
			padding: 0.5em 1em;
		}
		.loading {
			color: white;
			display: flex;
			justify-content: center;
		}
	}
}
</style>