<section class="col xfill acenter">
	<div class="col card">
		<div class="row title xfill">
			<div class="row acenter">
				<img class="profile" src="../img/rup1.jpg" alt="rup" />
				<h2>SERIE TRANSMEDIA?</h2>
			</div>
			<div>
				<h1>···</h1>
			</div>
		</div>
		<div class="row xfill">
			<img class="xfill" src="../img/what.gif" alt="what?" />
		</div>
		<div class="row likes xfill acenter">
			<img src="../img/liked.svg" alt="" />
			<p>Youplanet y 24 productoras más</p>
		</div>
		<xdiv />
		<div class="row cta xfill acenter">
			<div class="row fcenter">
				<img src="../img/like.svg" alt="" />
				<p>Me gusta</p>
			</div>
			<div class="row fcenter">
				<img src="../img/comment.svg" alt="" />
				<p>Comentar</p>
			</div>
		</div>
		<xdiv />
		<div class="row desc xfill acenter">
			<p>
				Grande Fronteo es un proyecto pensado para formato de serie. Donde la audiencia puede
				interactuar directamente con los personajes ficticios que aparecen, a través de las redes
				sociales. <br /><br />A su vez, personas reales, del mundo del stream y de redes sociales,
				aparecen en la série interpretándose a ellos mismos e interactuando con los personajes
				ficticios, rompiendo la barrera entre realidad y ficción en todo momento.
			</p>
		</div>
		<xdiv />
		<div class="row comments xfill atop">
			<img src="../img/ibai.jpg" alt="" />
			<div class="col">
				<h4>Ibai</h4>
				<p>De locos! Cuándo sale??</p>
			</div>
		</div>
		<div class="row commenting xfill acenter">
			<img src="../img/manu.jpg" alt="" />
			<p>Escribe un comentario</p>
		</div>
	</div>
</section>

<style lang="scss">
	section {
		height: 100vh;
		background: #ff005f;
		color: #1a1a1a;
		.card {
			background: white;
			width: 90vw;
			max-width: 800px;
			border-radius: 20px;
			overflow: hidden;
			.title {
				justify-content: space-between;
				padding: 10px 15px;
				.row {
					gap: 10px;
					.profile {
						width: 50px;
						height: 50px;
						border-radius: 100%;
					}
				}
				h1 {
					color: #b5b5b5;
				}
			}
			xdiv {
				background: #cfcfcfb5;
			}
			.likes {
				padding: 10px;
				gap: 5px;
				img {
					width: 18px;
					height: 18px;
				}
			}

			.cta {
				padding: 5px 10px;
				.row {
					width: 50%;
					gap: 10px;
					padding: 5px 10px;
					font-weight: bold;
					border-radius: 10px;
					&:hover {
						background: #e7e7e7;
					}
					img {
						height: 20px;
					}
				}
			}
			.desc {
				padding: 20px;
				font-size: 15px;
				p {
					hyphens: auto;
					text-align: justify;
				}
			}
			.comments {
				padding: 10px;
				gap: 5px;
				img {
					height: 30px;
					width: 30px;
					border-radius: 50%;
				}
				.col {
					background: #f0f2f5;
					padding: 5px 15px;
					border-radius: 15px;
				}
			}
            .commenting {
                padding: 10px;
                gap: 5px;
                img {
                    width: 40px;
                    height: 40px;
                    border-radius: 50px;
                }
                p {
                    width: 92%;
                    background-color: #f0f2f5;
                    padding: 5px 15px;
					border-radius: 15px;
                }
            }
		}
	}
</style>
