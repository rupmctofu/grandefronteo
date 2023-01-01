<section class="col xfill fcenter">
	<div class="row post">
		<div class="col">
			<img src="./img/post1.jpg" alt="" />
		</div>
		<div class="col itext">
			<div class="row xfill acenter">
				<img class="gfprofile" src="./img/gf-profile.svg" alt="" />
				<h2>SINOPSIS</h2>
			</div>
			<div class="row">
				<p>
					A Tomás y a Jonathan los acaban de echar del piso de su abuela, donde vivían del free.
					Necesitan conseguir 20k para pagar el impuesto de sucesiones y tienen 6 meses para
					conseguirlo. Así que ahora mismo están #homeless. <br /><br />Por p*ta casualidad,
					encuentran una wallet de bitcoins (o vete tú a saber de qué), pero está protegida por
					huella dactilar y no pueden acceder.<br /><br />Y se les ocurre la genial idea de
					encontrar al dueño por vía de las redes sociales, para conseguir acceder al dinero y
					recuperar su piso. <br /><br /><span>#grandefronteo #serie #transmedia</span>
				</p>
			</div>
			<div class="row xfill cta">
				<div>
					<img src="./img/ilike.svg" alt="" />
					<img src="./img/icomment.svg" alt="" />
					<img src="./img/isend.svg" alt="" />
				</div>
				<img src="./img/isave.svg" alt="" />
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	section {
		height: 100vh;
		width: 100vw;
		background: #ff005f;
		.post {
			width: 70vw;
			min-width: 900px;
			height: auto;
			background: white;
			border-radius: 30px;
			overflow: hidden;
			.col {
				width: 50%;
				gap: 10px;
				img {
					width: 100%;
				}
				.gfprofile {
					height: 40px;
					width: 40px;
				}
			}
			.itext {
				padding: 15px;
				p {
					text-align: justify;
                    hyphens: auto;
                    span {
                        color: #3fa9f5;
                    }
				}
			}
			.cta {
                justify-content: space-between;
                div {
                    gap: 15px;
                }
				img {
					height: 20px;
					width: 20px;
				}
			}
		}
	}
</style>
