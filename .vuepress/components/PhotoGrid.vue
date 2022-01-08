<template>
	<ul id="photo-list">
		<div class="photo-container">
			<video playsinline autoplay muted loop poster="/upload/photos/poster.jpg" class="full-size">
				<source src="/upload/photos/Canyon.mp4" type="video/mp4">
			</video>
		</div>
		<div class="photo-container">
			<img class="half-size" src="/upload/photos/tall.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		<div class="photo-container">
			<img class="half-size" src="/upload/photos/DSC06100.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		<div class="photo-container">
			<img class="full-size" src="/upload/photos/DSC01636.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		<div class="photo-container">
			<video class="half-size" playsinline autoplay muted loop>
				<source src="/upload/photos/Lake.mp4" type="video/mp4">
			</video>
		</div>
		<div class="photo-container">
			<img class="half-size" src="/upload/photos/DSC01586.jpg" alt="Rock Climbing.">
		</div>
				<div class="photo-container">
			<img class="" src="/upload/photos/DSC00331.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		<div class="photo-container">
			<img class="half-size" src="/upload/photos/DSC00838.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		<div class="photo-container"> <img class="half-size" src="/upload/photos/DSC01000.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away."> </div>
		<div class="photo-container">
			<img class="full-size bigger" src="/upload/photos/DSC00236.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		<div class="photo-container">
			<img class="half-size" src="/upload/photos/DSC00075.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
				<div class="photo-container">
			<img class="half-size" src="/upload/photos/rmnp.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
				<div class="photo-container">
			<img class="full-size" src="/upload/photos/DSC03401.jpg"
				alt="A photo of sand dunes, with people at the top shot from far away.">
		</div>
		
	</ul>
</template>

<script>
  export default {
  	methods: {
  		identifyImages: function () {
  			let images = document.getElementById("photo-list").children;
  			for (let i = 0; i < images.length; i++) {

  				let height = images[i].children[0].naturalHeight;
  				let width = images[i].children[0].naturalWidth;
  				if (height > width) {
  					images[i].children[0].classList.add("half-size")
  				} else if (height < width) {
  					images[i].children[0].classList.add("full-size")
  				} else {
  					images[i].children[0].classList.add("half-size")
  				}

					console.log(images[i].children[0].naturalHeight)
  			}
				document.addEventListener('contextmenu', event => event.preventDefault());


  		}
  	}
  }
</script>

<style scoped>

#photo-list {
	max-width: 800px;
	margin: auto;
}

#photo-list video {
	object-fit: cover;
	object-position: bottom;
	border-radius: 0px;
	height: 500px;
}

.photo-container {
	display: inline;
	width: 100%;
	position: relative;
}

.photo-container img {
	object-fit: cover;
	margin: auto;
	border-radius: 0px;
	pointer-events: none;
}

.half-size {
	width: calc(50% - 3px);
	height: 500px;
}

.full-size {
	width: calc(100% - 2px) !important;
	max-height: 420px;
}

.full-size.bigger {
	max-height: 600px;
}

@media screen and (max-width: 680px){
	/* .half-size, .full-size {
		width: 100%;
	} */

	#photo-list {
		padding-left: .2rem;
		padding-right: .12rem
	}

	.half-size, #photo-list video {
	height: 300px;
}

.full-size {
	width: 99.6% !important;
}

}





</style>
