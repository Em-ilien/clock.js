<script>
	let secondsHandTransform = 0;
	setInterval(() => {
		secondsHandTransform += 6;
	}, 1000);
</script>

<div class="clock-ctn">
	<div class="clock">
		<div class="seconds-hand-ctn hand-ctn" style:transform={`rotate(${secondsHandTransform}deg)`}>
			<div class="seconds-hand hand"></div>
		</div>
		<div
			class="minutes-hand-ctn hand-ctn"
			style:transform={`rotate(${secondsHandTransform / 60}deg)`}
		>
			<div class="minutes-hand hand"></div>
		</div>
		<div
			class="hours-hand-ctn hand-ctn"
			style:transform={`rotate(${secondsHandTransform / 3600}deg)`}
		>
			<div class="hours-hand hand"></div>
		</div>
		<div class="center"></div>
	</div>
</div>

<style>
	.clock-ctn {
		width: calc(min(100vh, 100vw) - 1em);
		height: calc(min(100vh, 100vw) - 1em);
	}

	.clock {
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 3rem;
		font-family: monospace;
		border-radius: 50%;
		border: 5px solid black;
		width: calc(100% - 2 * 5px);
		height: calc(100% - 2 * 5px);
	}

	.hand-ctn {
		height: calc(min(100vh, 100vw));
		display: flex;
		justify-content: center;
		align-items: flex-start;
		position: absolute;
	}

	.hand {
		width: 50%;
		border-radius: 16px;
	}

	.seconds-hand-ctn {
		background-color: #ff000005;
		width: 20px;
	}

	.seconds-hand {
		background-color: rgb(255, 0, 0);
		height: 50%;
		transform: translateY(calc(0% + 0.5em));
	}

	.minutes-hand-ctn {
		background-color: #00ff0005;
		width: 30px;
	}

	.minutes-hand {
		background-color: #000000;
		height: 40%;
		transform: translateY(calc(20% + 0.5em));
	}

	.hours-hand-ctn {
		background-color: #0000ff05;
		width: 40px;
	}

	.hours-hand {
		background-color: #000000;
		height: 30%;
		transform: translateY(calc(60% + 0.5em));
	}

	.center {
		width: 0.75em;
		height: 0.75em;
		background-color: #000000;
		border-radius: 50%;
		position: absolute;
	}
</style>
