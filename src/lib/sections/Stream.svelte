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

<section class="col fcenter">
	<div class="row acenter">
		<video
			class="fill"
			poster="../img/landing-bg.jpg"
			src="../img/teaser.mp4"
			bind:duration
			bind:paused
			playsinline
		>
			<track kind="captions" />
		</video>

		<div class="col land-left jcenter yfill">
			<img class="xfill" src="/img/landing-logo.svg" alt="Grande Fronteo logo" />

			<p class="description">
				Tomás ha encontrado una billetera de criptomonedas pero no sabe de quién es. Así que para
				llegar hasta él, idea un plan un tanto peculiar.
			</p>

			<div class="cta row acenter">
				<a href="/#" class="leer btn">
					<span>Leer Guión</span>
				</a>

				<a href="/#" class="more-info btn row acenter nowrap">
					<img src="/img/i.svg" alt="Info" />
					<span>Más información</span>
				</a>
			</div>
		</div>

		<div class="col land-right">
			<button class="play" on:click={playVideo}>Play</button>
		</div>
	</div>
</section>

<style lang="scss">
	section {
		background: #ff005f;
		height: 100vh;
		width: 100vw;
		.row {
			position: relative;
			height: 85%;
			width: 85%;
			border-radius: 50px;
			overflow: hidden;
			*:not(video) {
				z-index: 1;
			}
			video {
				inset: 0;
				position: absolute;
				top: 0;
				left: 0;
			}

			.land-left {
				width: 40%;
				background: linear-gradient(to right, rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0));
				padding: 50px;

				img {
					max-width: 600px;
				}

				.description {
					max-width: 500px;
					margin-top: 20px;
					color: #fff;
				}

				.cta {
					gap: 10px;
					margin-top: 20px;

					a {
						height: 40px;
						font-size: 14px;
						font-weight: bold;
						border: none;
						border-radius: 3px;
						padding-left: 16px;
						padding-right: 16px;

						span {
							margin-bottom: -4px;
						}
					}

					.leer {
						background: #fff;
					}

					.more-info {
						gap: 6px;
						background: rgba(#fff, 0.6);
						color: #fff;

						img {
							width: 20px;
						}
					}
				}
			}

			.land-right {
				.play {
					color: white;
				}
			}
		}
	}
</style>
