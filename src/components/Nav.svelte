<script>
	import enkoder from "../assets/images/enkoder.png";

	export let segment;
	// export const elements = [
	// 	{endpoint: 'enkoder', label: 'Enkoder' },
	// ]
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 2.3em);
		height: 2px;
		background-color: #FE8104;
		display: block;
		bottom: -1px;
	}

	a {
		font-weight: 450;
		text-decoration: none;
		text-align: center;
		padding: 15px 18px;
		display: block;
	}

	a:hover {
		color: #FE8104;
	}
	
	.img-div {
		padding: 15px 25px;
	}

	img:hover {
		cursor: pointer;
	}
</style>

<nav>
	<ul>
		<li><div class="img-div"><img alt="Enkoder" src="{enkoder}" height="40px"></div></li>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About us</a></li>
		<!-- {#each elements as element}
			<li>
				<a aria-current="{segment === element.endpoint ? 'page' : undefined}" href='{element.endpoint}'>{element.label}</a>
			</li>
		{/each} -->
		<li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li>
	</ul>
</nav>
