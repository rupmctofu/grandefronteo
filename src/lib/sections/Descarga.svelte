<section class="col xfill fcenter">
	<div class="col card jcenter">
		<div class="row acenter xfill">
			<h3>Tu saldo</h3>
			<div class="row saldo">
				<img src="./img/coin.svg" alt="" />
				<p>35</p>
			</div>
			<div class="btn">X</div>
		</div>
		<xdiv />
		<div class="row row-premios">
			<div class="premio col">
				<div class="col square fcenter xfill">
					<img src="./img/page.svg" alt="" />
					<div class="row price acenter">
						<img src="./img/coin.svg" alt="" />
						<p>5</p>
					</div>
				</div>
				<p>Desbloquea una página de guión</p>
			</div>
			<div class="premio col">
				<div class="col square fcenter xfill">
					<img src="./img/page.svg" alt="" />
					<div class="row price acenter">
						<img src="./img/coin.svg" alt="" />
						<p>5</p>
					</div>
				</div>
				<p>Desbloquea una página de guión</p>
			</div>
			<div class="premio col">
				<div class="col square fcenter xfill">
					<img src="./img/page.svg" alt="" />
					<div class="row price acenter">
						<img src="./img/coin.svg" alt="" />
						<p>5</p>
					</div>
				</div>
				<p>Desbloquea una página de guión</p>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	section {
		height: 100vh;
		width: 100vw;
		background: #f2f2f2;
		.card {
			background: white;
			border-radius: 5px;
			padding: 30px;
			.saldo {
				background: rgba($color: black, $alpha: 0.2);
			}
			.btn {
				align-self: flex-end;
			}
            .row-premios {

                gap: 10px;
            }
            .premio {
                gap: 5px;
                width: 150px;
            }
			.square {
                background: #8205b4;
                height: 150px;
                width: 150px;
                padding: 30px;
                border-radius: 5px;
                gap: 15px;

                img {
                    height: 40px;
                }
                .price {
                    background: rgba($color: black, $alpha: 0.2);
                    padding: 7px 15px;
                    border-radius: 5px;
                    gap: 5px;
                    img {
                        height: 15px;
                    }
                    p {
                        font-size: 16px;
                        color: white;
                    }
                }
			}
		}
	}
</style>
