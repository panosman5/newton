
<style>
input[type="submit"],
	input[type="reset"],
	input[type="button"],
	.button {
		-moz-appearance: none;
		-webkit-appearance: none;
		-ms-appearance: none;
		appearance: none;
		-moz-transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out;
		-webkit-transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out;
		-ms-transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out;
		transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out;
		background-color: transparent;
		border: 0;
		border: solid 2px #7f7f7f;
		border-radius: 0 !important;
		color: #7f7f7f !important;
		cursor: pointer;
		display: inline-block;
		font-family: "Montserrat", Helvetica, sans-serif;
		font-weight: 700;
		height: 3em;
		height: calc(3em + 2px);
		letter-spacing: 0.05em;
		line-height: 3em;
		padding: 0 1.25em;
		text-align: center;
		text-decoration: none;
		text-transform: uppercase;
		white-space: nowrap;
	}

		input[type="submit"]:hover,
		input[type="reset"]:hover,
		input[type="button"]:hover,
		.button:hover {
			background-color: rgba(144, 144, 144, 0.075);
		}

		input[type="submit"]:active,
		input[type="reset"]:active,
		input[type="button"]:active,
		.button:active {
			background-color: rgba(144, 144, 144, 0.2);
		}

		input[type="submit"].icon,
		input[type="reset"].icon,
		input[type="button"].icon,
		.button.icon {
			padding: 0 1.25em 0 1.35em;
		}

			input[type="submit"].icon:before,
			input[type="reset"].icon:before,
			input[type="button"].icon:before,
			.button.icon:before {
				margin: 0 0.5em 0 0;
			}

		input[type="submit"].icon-after,
		input[type="reset"].icon-after,
		input[type="button"].icon-after,
		.button.icon-after {
			padding: 0 1.35em 0 1.25em;
		}

			input[type="submit"].icon-after:before,
			input[type="reset"].icon-after:before,
			input[type="button"].icon-after:before,
			.button.icon-after:before {
				float: right;
				line-height: inherit;
				margin: 0 0 0 0.75em;
			}

		input[type="submit"].fit,
		input[type="reset"].fit,
		input[type="button"].fit,
		.button.fit {
			width: 100%;
		}

		input[type="submit"].small,
		input[type="reset"].small,
		input[type="button"].small,
		.button.small {
			font-size: 0.8em;
		}

		input[type="submit"].large,
		input[type="reset"].large,
		input[type="button"].large,
		.button.large {
			font-size: 1.35em;
		}

		input[type="submit"].primary,
		input[type="reset"].primary,
		input[type="button"].primary,
		.button.primary {
			background-color: #7bceba;
			border: 0;
			color: #ffffff !important;
			height: 3em;
		}

			input[type="submit"].primary:hover,
			input[type="reset"].primary:hover,
			input[type="button"].primary:hover,
			.button.primary:hover {
				background-color: #8ed5c4;
			}

			input[type="submit"].primary:active,
			input[type="reset"].primary:active,
			input[type="button"].primary:active,
			.button.primary:active {
				background-color: #68c7b0;
			}

		input[type="submit"].disabled, input[type="submit"]:disabled,
		input[type="reset"].disabled,
		input[type="reset"]:disabled,
		input[type="button"].disabled,
		input[type="button"]:disabled,
		.button.disabled,
		.button:disabled {
			background-color: #868686 !important;
			border: 0;
			color: #f5f5f5 !important;
			cursor: default;
			height: 3em;
			opacity: 0.25;
		}
</style>