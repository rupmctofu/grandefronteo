<section class="col xfill fcenter">
	<div class="col">
		<div class="speech-wrapper">
			<!--  Preegunta -->
			<div class="bubble">
				<div class="txt">
					<p class="name">Tú</p>
					<div class="row acenter">
						<p class="message">... pero qué tienes?</p>
						<img src="./img/ghost.svg" alt="" />
					</div>
				</div>
				<div class="bubble-arrow" />
			</div>
			<!--  RESPOSTA -->
			<div class="bubble alt">
				<div class="txt">
					<p class="name alt">Robert</p>
					<p class="message">Tengo un guión</p>
				</div>
				<div class="bubble-arrow alt" />
			</div>
			<!--  GIF -->
			<div class="bubble gif alt">
				<img src="./img/sunglasses.gif" alt="" />
			</div>
			<!--  Preegunta -->
			<div class="bubble">
				<div class="txt">
					<p class="name">Tú</p>
					<p class="message">Es muy largo?</p>
				</div>
				<div class="bubble-arrow" />
			</div>
			<!--  RESPOSTA -->
			<div class="bubble alt">
				<div class="txt">
					<p class="name alt">Robert</p>
					<p class="message">Unas 40 páginas</p>
				</div>
				<div class="bubble-arrow alt" />
			</div>
			<!--  Preegunta -->
			<div class="bubble">
				<div class="txt">
					<p class="name">Tú</p>
					<p class="message">Hazme un resumen</p>
				</div>
				<div class="bubble-arrow" />
			</div>
			<!--  RESPOSTA -->
			<div class="bubble alt">
				<div class="txt">
					<p class="name alt">Robert</p>
					<img src="./img/finger.svg" alt="" />
				</div>
				<div class="bubble-arrow alt" />
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	section {
		width: 100vw;
		height: 100vh;
		background: url('../img/wa-bg.jpg') no-repeat;
		background-size: cover;
		background-position: center;
		.speech-wrapper {
			padding: 30px 40px;
			.bubble {
				width: auto;
				height: auto;
				display: block;
				background: #343c42;
				border-radius: 4px;
				box-shadow: 2px 8px 15px rgba($color: black, $alpha: 0.5);
				position: relative;
				margin: 0 0 25px;
				&.alt {
					margin: 0 0 0 60px;
					background: #074540;
				}
				.txt {
					padding: 8px 55px 8px 14px;
					.name {
						font-weight: 600;
						font-size: 12px;
						margin: 0 0 4px;
						color: #3498db;

						span {
							font-weight: normal;
							color: #b3b3b3;
						}
						&.alt {
							color: #2ecc71;
						}
					}
					.row {
						gap: 5px;
						img {
							height: 20px;
						}
					}
					.message {
						font-size: 14px;
						margin: 0;
						color: #e6e6e6;
					}
					.timestamp {
						font-size: 11px;
						position: absolute;
						bottom: 8px;
						right: 10px;
						text-transform: uppercase;
						color: #999;
					}
				}
				.bubble-arrow {
					position: absolute;
					width: 0;
					bottom: 42px;
					left: -16px;
					height: 0;
					&.alt {
						right: -2px;
						bottom: 40px;
						left: auto;
					}
				}
				.bubble-arrow:after {
					content: '';
					position: absolute;
					border: 0 solid transparent;
					border-top: 9px solid #343c42;
					border-radius: 0 20px 0;
					width: 15px;
					height: 30px;
					transform: rotate(145deg);
				}
				.bubble-arrow.alt:after {
					transform: rotate(45deg) scaleY(-1);
					border-top: 9px solid #074540;
				}
                img {
							height: 20px;
						}
			}
			.gif {
				margin-top: 10px !important;
				padding: 5px !important;
				img {
					width: 250px;
					height: 100%;
				}
			}
		}
	}
</style>
