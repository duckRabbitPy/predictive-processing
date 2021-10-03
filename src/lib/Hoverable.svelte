<script>
	let hovering = false

	function enter() {
		hovering = true;
	}

</script>

<div on:mouseenter={enter}>
	<slot hovering={hovering}></slot>
</div>