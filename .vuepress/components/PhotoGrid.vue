<template>
	<div>
		<div class="Profile">
			<div class="container grid">
				<div class="grid-descrip-left">
					<div class="description">
						<h3>Top of Trail Ridge Road</h3>
						<p>
							An incredible drive with some crazy views. Nickki and I drove from Grand Lake to the other side on Estes Park on our way home from our camping trip. Bring a jacket 🥶
						</p>
					</div>
					<img class="grid-image" src="/upload/photos/DSC03401.jpg"
						alt="A photo of sand dunes, with people at the top shot from far away.">
				</div>
				<div class="grid-descrip-right">
					<img class="grid-image" src="/upload/photos/DSC00191.jpg"
						alt="A photo of sand dunes, with people at the top shot from far away.">
					<div class="description">
						<h3>The Great Sand Dunes located near Alamosa, Colorado. </h3>
						<p>
							A four hour drive from Denver and an international dark sky spot, The Sand Dunes is an incredible place
							with some stunning, other world views. Bring water 💦
						</p>
					</div>
				</div>
				<div class="grid-descrip-left">
					<div class="description">
						<h3>Gunnison, Colorado</h3>
						<p>
							Spitz brought me here, pretty sure he works here or something. These incredible rock formations can be
							found near The Blue Mesa Resivor. Do not bring a JBL speaker 🔇
						</p>
					</div>
					<img class="grid-image" src="/upload/photos/_DSC0123.jpg">
				</div>
							<div class="grid-descrip-right">
					<img class="grid-image" src="/upload/photos/DSC07020.jpg"
						alt="A photo of sand dunes, with people at the top shot from far away.">
					<div class="description">
						<h3>South Baldy Peak</h3>
						<p>
							For my 27th birthday, I along with 7 of my closest friends took a long hike up upto South Baldy Peak where he got sunburned and wind whipped. Ten out of ten would do it again. Bring the homies 💁🏻‍♂️
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>

.Profile {
	padding: 3rem;
	margin-top: 7rem;

}

.grid-descrip-right .description {
	margin: auto;
	padding-left: 3rem;
}

.grid-descrip-left .description {
	margin: auto;
	padding-right: 3rem;
}

.container.grid {
	display: grid;
	grid-template-columns: 1fr;
	max-width: 1200px;
	margin: auto;
	overflow: scroll;
}

.grid-descrip-right {
	display: grid;
	grid-template-columns: 2fr 1fr;
}

.grid-descrip-left {
	display: grid;
	grid-template-columns: 1fr 2fr;
}



.grid {
	display: grid;
	grid-template-columns: 1fr;
	overflow: scroll;
}

.grid-image {
	margin: 4rem 0rem 4rem 0rem
}

	.grid .grid-image {
		display: flex;
		align-items: center;
	}

	.profile-grid {
		display: grid;
		grid-template-columns: 1fr 3fr;
		margin-top: 8rem;
	}

	#seemore {
		position: absolute;
		bottom: 0%;
		left: 0%;
		color: #fff;
		font-size: 10rem;
	}

	@media screen and (max-width: 728px) { 
		.grid-image { 
			background-position: center;
			background-size:contain;
		 }

	}

	@media screen and (max-width: 768px) { 

			.grid-image {
				margin: 0;
			}

.grid-descrip-right {
	display: flex;
	grid-template-columns: 1fr;
		  flex-direction: column;

	
}

.grid-descrip-left {
	display: flex;
	grid-template-columns:1fr;
	  flex-direction: column-reverse;
}

.grid-descrip-right .description {
	margin: auto;
	padding-left: 0rem;
}

.grid-descrip-left .description {
	margin: auto;
	padding-right: 0rem;
}


	}




</style>
