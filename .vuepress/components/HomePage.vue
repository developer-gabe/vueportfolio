<template>
	<div class="home-page">
		<h4 class="subheader">{{time}}. {{greeting}}.</h4>
		<h1>Gabe Sousa</h1>
				<ul class="navigation-list"> 
					<li> 
					 <router-link to="/journal">Dev. Journal </router-link>
					</li>
					<li> 
					 <router-link to="/photography">Photography </router-link>
					</li>
				</ul>
				<div id="social-grid">
					<a href="https://www.linkedin.com/in/gsous/" target="_blank"><img class="social-icon"
							src="/upload/linkedin.svg"></a>
					<a href="https://www.instagram.com/saucygsous" target="_blank"><img class="social-icon"
							src="/upload/instagram.svg"></a>
				</div>
			</div>
</template>

<script>
export default {
	data: function () {
		return {
			time: "",
			greeting: ""
		}
	},
	methods: {
		 updateTime: function () {
			 	var today = new Date()
			 	var curHr = today.getHours()

			 	if (curHr < 12) {
					 this.time = "Good Morning"
					 this.greeting = "Hello World"
			 	} else if (curHr < 18) {
			 		this.time = "Good Afternoon"
					this.greeting = "Drink water"
			 	} else {
			 	this.time = "Good Evening"
				 this.greeting = "Slack notifications off"
			 	}
	}
	},
	mounted() {
		this.updateTime()
	}
}
</script>

<style scoped>

	.home-page {
		margin: auto;
		text-align: center;
		position: absolute;
		top: 40%;
		left: 50%;
		opacity: 0;
		transform: translate(-50%, -50%);
		animation: fadeIn 1s ease-in-out .1s 1 forwards ;
		color: #fff;
		z-index: 10;
		width: 100%;
	}

	.subheader {
		margin: auto;
	}

	a {
		color: #fff;
	}

	.navigation-list {
		list-style: none;
	}

	.navigation-list li {
		display: inline-block;
		padding: 1rem;
	}

	#social-grid {
		text-align: center;
		display: grid;
		grid-template-columns: 50px 50px;
		grid-column-gap: 0px;
		margin: auto;
		justify-content: center;
	}

	.social-icon {
		max-width: 25px;
		display: block;
		margin: auto;
		padding-top: 1rem;
		transition: all 500ms cubic-bezier(0.25, 0.8, 0.25, 1);
	}

	.social-icon:hover {
		transform: scale(1.2);
	}

	@keyframes fadeIn {
		0% {
			opacity: 0;

		}

		100% {
			opacity: 1;
		}
	}

</style>