<script>
	export let open = false
</script>

<button class="cursor-pointer mr-4 border-none focus:outline-none" 
		class:open on:click={() => open = !open}>
	<svg width=25 height=20>
		<line id="top" x1=-100 y1=0  x2=26 y2=2/>
		<line id="middle" x1=0 y1=12 x2=22 y2=12/>
		<line id="bottom" x1=-100 y1=22 x2=26 y2=22/>
	</svg>
</button>

<style>
	svg {
		min-height: 24px;
		transition: transform 0.3s ease-in-out;
	}
	
	svg line {
		stroke: currentColor;
		stroke-width: 3;
		transition: transform 0.3s ease-in-out
	}
	
	button {
		z-index: 20;
	}
	
	.open svg {
		transform: scale(1)
	}
	
	.open #top {
		transform: translate(4px, 2px) rotate(45deg)
	}
	
	.open #middle {
		opacity: 0;
	}
	
  .open #bottom {
		transform: translate(-14px, 4px) rotate(-45deg)
	}
</style>