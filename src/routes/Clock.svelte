<script>
	let hours;
	let minutes;
	let seconds;

	setInterval(() => {
		computeHands();
	}, 1000);

	computeHands();

	function computeHands() {
		const now = new Date();
		hours = now.getHours();
		minutes = now.getMinutes();
		seconds = now.getSeconds();
	}
</script>

<div class="clock-ctn">
	<div class="clock">
		<div class="seconds-hand-ctn hand-ctn" style:transform={`rotate(${seconds * 6}deg)`}>
			<div class="seconds-hand hand"></div>
		</div>
		<div
			class="minutes-hand-ctn hand-ctn"
			style:transform={`rotate(${minutes * 6 + seconds / 10}deg)`}
		>
			<div class="minutes-hand hand"></div>
		</div>
		<div class="hours-hand-ctn hand-ctn" style:transform={`rotate(${hours * 30 + minutes / 2}deg)`}>
			<div class="hours-hand hand"></div>
		</div>
		<div class="center"></div>
	</div>
</div>

<style>
	.clock-ctn {
		width: calc(min(100vh, 100vw) - 3em);
		height: calc(min(100vh, 100vw) - 3em);
	}

	.clock {
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 3rem;
		font-family: monospace;
		border-radius: 50%;
		border: 15px solid black;
		width: calc(100% - 2 * 15px);
		height: calc(100% - 2 * 15px);
		background: #e8c9a957;
		background-image: url('clock.png');
		background-repeat: no-repeat;
		background-size: cover;
		box-shadow: 5px 5px 15px 3px rgba(0, 0, 0, 0.5);
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
		box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.5);
	}

	.seconds-hand-ctn {
		width: 10px;
		z-index: 3;
	}

	.seconds-hand {
		background-color: rgb(255, 0, 0);
		height: 40%;
		transform: translateY(calc(20% + 40px));
	}

	.minutes-hand-ctn {
		width: 25px;
		z-index: 2;
	}

	.minutes-hand {
		background-color: #000000;
		height: 30%;
		transform: translateY(calc(60% + 40px));
	}

	.hours-hand-ctn {
		width: 32.5px;
		z-index: 1;
	}

	.hours-hand {
		background-color: #000000;
		height: 20%;
		transform: translateY(calc(140% + 40px));
	}

	.center {
		width: 30px;
		height: 30px;
		background-color: #000000;
		border-radius: 50%;
		position: absolute;
		z-index: 4;
	}
</style>
