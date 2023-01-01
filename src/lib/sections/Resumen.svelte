<section class="col xfill fcenter">
	<h1>RESUMIENDO</h1>
	<div class="col content acenter">
		<img class="phone" src="./img/phone.png" alt="phone" />
		<div class="story col">
			<div class="row">
				<div class="col"></div>
				<div class="col"></div>
				<div class="col"></div>
				<div class="col"></div>
			</div>
			<img class="storypic" src="./img/story1.jpg" alt="" />
		</div>
	</div>
</section>

<style lang="scss">
	section {
		height: 100vh;
		width: 100vw;
		background: url('./img/glitch.jpg');
		position: relative;
		*:not(h1) {
			z-index: 1;
		}
		h1 {
			color: white;
			font-size: 200px;
			position: absolute;
			z-index: 0;
		}

		.content {
			height: 80vh;
			background: black;
			border-radius: 20px;
			overflow: hidden;

			.phone {
				position: absolute;
				height: 80vh;
				z-index: 2;
			}
			.story {
                position: absolute;
				height: 65vh;
				padding: 5px;
				.col {
					height: 3px;
					width: 24%;
					background-color: rgb(255, 0, 0);
				}

				.storypic {
					height: 100%;
				}

			}
		}
	}
</style>
