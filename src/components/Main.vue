<template>
	<main>
		<div class="container-60 my-5">
			<div class="row">
				<div class="col-3 offset-9 pb-3">
					<select v-model="selectedGenre" name="genre" id="genre" class="form-select" @change="filterCards">
						<option value="all">All</option>
						<option value="rock">Rock</option>
						<option value="pop">Pop</option>
						<option value="jazz">Jazz</option>
						<option value="metal">Metal</option>
					</select>
				</div>
			</div>
			<div v-if="filteredCards" class="row row-cols-5">
				<Card 
				v-for="(card, index) in filteredCards" :key="index" :image="card.poster" :name="card.title" :title="card.title" :artist="card.author" :year="card.year"/>
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
			filteredCards: null,
			selectedGenre: 'all',
			arrayOriginal: null,
		}
	},
	mounted() {
		setTimeout(() => {
			this.getCards();
		}, 1000);
	},
	computed: {
	},
	methods: {
		getCards () {
			axios.get('https://flynn.boolean.careers/exercises/api/array/music')
			.then((result) => {
				this.arrayOriginal = result.data.response;
				this.filteredCards = result.data.response;
				
			})
			.catch((error) => {
				console.log(error);
			})
		},
		filterCards() {
			//faccio vedere tutti gli album
			this.filteredCards = this.arrayOriginal;

			//se seleziono un genere diverso
			if (this.selectedGenre !== 'all') {
				this.filteredCards = this.filteredCards.filter(album => album.genre.toLowerCase()  === this.selectedGenre);
			} else {
				return this.filteredCards;
			}
			return this.filteredCards;
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