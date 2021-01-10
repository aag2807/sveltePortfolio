<script>
	// your script goes here #673ab7
</script>

<style lang='scss'>
	  $primary: #222831;
  $secondary: #393e46;

.box {
	display:flex;
	flex-direction: column;
	justify-content: center;
}

	.main {
		display: flex;
		width:200px;
		justify-content: space-between;
		align-self: center;
		align-content: center;
		align-items: center;
	}

	.circle {
		width: 20px;
		height: 20px;
		background: linear-gradient(#222831 , #393e46);
		border-radius: 50%;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.circle:before {
		content: "";
		width:20px;
		height:20px;
		background: linear-gradient(#222831 , #393e46);
		border-radius: 50%;
		opacity: 0.7;
		animation: loading 2s;
		animation-iteration-count: infinite;

	}
	
	@keyframes loading {
		100% {
			transform: scale(3);
			opacity: 0;
		}
	}

	.circle:nth-child(2){
		animation-delay:  0.3s;
	}

	.circle:nth-child(3){
		animation-delay:  0.6s;
	}

	.circle:nth-child(4){
		animation-delay:  0.9s;
	}

	.circle:nth-child(5){
		animation-delay:  1.2s;
	}


</style>
<div class="box">
	<div class="main">
		<div class="circle"></div>
		<div class="circle"></div>
		<div class="circle"></div>
		<div class="circle"></div>
		<div class="circle"></div>
	</div>
</div>

