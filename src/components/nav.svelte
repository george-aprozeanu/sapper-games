<script>
	export let segment;
</script>

<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href="games/tetris">Tetris</a></li>
	</ul>
</nav>
