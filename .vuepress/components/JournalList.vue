<template>
  <div class="inner-journal-list">
  	<div v-for="post in journal" :key="post.title" class="post">
			<router-link tag="a" :to="post.path">
			<div class="post-content">
  		<h3 class="title">{{ post.frontmatter.title }}</h3>
  		<p class="excerpt">{{ post.frontmatter.excerpt }}</p>
  		<p class="reading-time">{{post.readingTime.text}}</p>
			</div>
			</router-link>
  	</div>
  </div>
</template>

<script>
  export default {
  	computed: {
  		journal() {
  			return this.$site.pages
  				.filter(x => x.path.startsWith('/journal/') && !x.frontmatter.journal_index)
  				.sort((a, b) => new Date(b.frontmatter.date) - new Date(a.frontmatter.date))
			}
		},
		methods:{
		}
  }
</script>

<style scoped>

	.inner-journal-list {
		margin: auto;
		max-width: 800px;
		display: grid;
		grid-template-columns: 1fr 1fr;
		padding-bottom: 4rem;
	}

	.title {
		cursor: pointer;
		font-weight: 600;
		font-size: 2.25rem;
		color: #000;
		padding-bottom: .25rem;
		transition: color ease-in-out 250ms;
	}

	.excerpt {
		font-size: 1rem;
		max-width: 80%;
		letter-spacing: .2px;
		width: 100%;

	}

	.post {
		display: flex;
		align-items: center;
		margin: .25rem;
		padding: 2rem;
		background: rgb(197, 222, 255);
		transition: all 500ms cubic-bezier(0.25, 0.8, 0.25, 1);
	}

	.inner-journal-list:nth-last-row {
		grid-template-columns: 1fr;
	}

	.post:hover .title {
		color: #0075e9;
	}

	.post .excerpt {
		color: #000;
	}

	.post:last-of-type {
		border: 0;
	}

	.post h2 {
		margin: 0;
	}

	.post h2:hover {
		cursor: pointer;
	}

	.post p {
		margin: 0;
		color: #000;
	}

	.reading-time {
		font-weight: 800;
		font-family: avenir;
		font-size: .9rem;
		padding-top: .5rem;
	}

	p.reading-time {
		color: #000;
	}


	@media screen and (max-width: 728px) {
		.inner-journal-list {
			display: block;
			grid-template-columns: 1fr;
		}

	}

</style>
