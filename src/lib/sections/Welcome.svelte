<script>
	let duration, showControlsTimeout, lastMouseDown;
	let time = 0;
	let paused = true;
	let showControls = true;

	function playVideo() {
		paused = !paused;
	}

	function handleMove(e) {
		clearTimeout(showControlsTimeout);
		showControlsTimeout = setTimeout(() => (showControls = false), 2500);
		showControls = true;

		if (!duration) return;
		if (e.type !== 'touchmove' && !(e.buttons & 1)) return;

		const clientX = e.type === 'touchmove' ? e.touches[0].clientX : e.clientX;
		const { left, right } = this.getBoundingClientRect();
		time = (duration * (clientX - left)) / (right - left);
	}

	function handleMousedown(e) {
		lastMouseDown = new Date();
	}

	function handleMouseup(e) {
		if (new Date() - lastMouseDown < 300) {
			if (paused) e.target.play();
			else e.target.pause();
		}
	}

	function format(seconds) {
		if (isNaN(seconds)) return '...';

		const minutes = Math.floor(seconds / 60);
		seconds = Math.floor(seconds % 60);
		if (seconds < 10) seconds = '0' + seconds;

		return `${minutes}:${seconds}`;
	}
</script>

<section class="col acenter fill">
	<video
		class="fill"
		poster="../img/landing-bg.jpg"
		src="../img/teaser.mp4"
		bind:duration
		bind:paused
		playsinline
	>
	<track kind="captions">
	</video>

	<div class="col land-left jcenter">
		<div class="container">
			<img src="../img/landing-logo.svg" alt="grande-fronteo-logo" />
			<p>
				Tomás ha encontrado una billetera de criptomonedas pero no sabe de quién es. Así que para
				llegar hasta él, idea un plan un tanto peculiar.
			</p>
			<div class="row acenter">
				<div class="btn leer">Leer Guión</div>
				<div class="btn info acenter"><img src="../img/i.svg" alt="" />Más información</div>
				<button class="btn play" on:click={playVideo}>Play</button>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	section {
		video {
			position: fixed;
			right: 0;
			bottom: 0;
		}

		.land-left {
			position: fixed;
			top: 0;
			padding: 50px;
			display: flex;
			background: linear-gradient(to right, rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0));
			height: 100vh;
			width: 100vw;

			.container {
				width: 40vw;
				max-width: 600px;
				min-width: 300px;

				p {
					margin-top: 20px;
					color: white;
					font-size: 14px;
				}

				.row {
					margin-top: 20px;
					display: flex;

					.btn {
						border: none;
						border-radius: 3px;
						padding: 6px 13px;
						font-weight: bold;
					}

					.leer {
						background-color: white;
						color: black;
					}

					.info {
						display: flex;
						background-color: rgba($color: white, $alpha: 0.6);
						color: white;
						margin-left: 5px;

						img {
							height: 15px;
							width: 15px;
							margin-right: 5px;
						}
					}
					
					.play {
						color: white;
					}
				}
			}
		}
	}
</style>
