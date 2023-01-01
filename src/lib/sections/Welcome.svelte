<section class="col fcenter fill">
	<video class="fill" playsinline autoplay loop muted>
		<source src="../img/bg.mp4" />
	</video>
	<img src="/img/landing-logo.svg" alt="" />
</section>


<style lang="scss">
	section {
		position: relative;
		width: 100vw;
		height: 80vh;
		background: black;

		*:not(video) {
			z-index: 1;
		}
		video {
			position: absolute;
			top: 0;
			left: 0;
			inset: 0;
		}
		img {
			max-width: 400px;
		}
	}
</style>
