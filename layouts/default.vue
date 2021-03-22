<template>
  <div>
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<style>
#page-wrapper {
		padding-top: 4.5em;
	} 
.container {
		margin: 0 auto;
		width: 1400px;
	}

		.container.medium {
			width: 1050px;
		}

		@media screen and (max-width: 1680px) {

			.container {
				width: 1200px;
			}

				.container.medium {
					width: 900px;
				}

		}

		@media screen and (max-width: 1280px) {

			.container {
				width: 960px;
			}

				.container.medium {
					width: 720px;
				}

		}

		@media screen and (max-width: 980px) {

			.container {
				width: 90%;
			}

				.container.medium {
					width: 67.5%;
				}

		}

		@media screen and (max-width: 736px) {

			.container {
				width: 90%;
			}

				.container.medium {
					width: 90%;
				}
    }

    .image {
		border: 0;
		display: inline-block;
		position: relative;
	}

		.image img {
			display: block;
		}

		.image.left {
			float: left;
			padding: 0 1.5em 1em 0;
			top: 0.25em;
		}

		.image.right {
			float: right;
			padding: 0 0 1em 1.5em;
			top: 0.25em;
		}

		.image.left, .image.right {
			max-width: 40%;
		}

			.image.left img, .image.right img {
				width: 100%;
			}

		.image.fit {
			display: block;
			margin: 0 0 2em 0;
			width: 100%;
		}

			.image.fit img {
				width: 100%;
			}

		.image.style1 {
			background: #ffffff;
			border-radius: 0.5em;
			border: solid 2em #ffffff;
			box-shadow: 0 2px 0 0 rgba(0, 0, 0, 0.125);
			margin-top: -0.25em;
		}

			.image.style1:after {
				background: #f0f0f0;
				border-radius: 100%;
				content: '';
				display: block;
				height: 0.75em;
				margin: -0.5em 0.5em 0 0;
				position: absolute;
				right: -2em;
				top: 50%;
				width: 0.75em;
			}

		.image.style2 {
			background: rgba(144, 144, 144, 0.2);
			border-radius: 0%;
			height: 100%;
			width: auto;
			overflow: hidden;
		}

			.image.style2 img {
				border-radius: 0%;
				object-fit: cover;
			}

</style>
