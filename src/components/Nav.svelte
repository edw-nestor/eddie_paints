<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
		background-color: rgb(236,236,235);
	}

	img {
		margin-top: 14px;
		margin-right: 13px;
		float: right;
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
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
	h2 {
		margin-top: 13px;
		margin-right: 60px;
		float: right;
		color: rgb(255,62,0);
	}
</style>

<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">EddiePaints.com</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About Eddie</a></li>
		<li><a aria-current="{segment === 'work' ? 'page' : undefined}" href="work">Eddie's Work</a></li>
		<li><a aria-current="{segment === 'praise' ? 'page' : undefined}" href="praise">Praise for Eddie</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">Eddie's Blog</a></li>
		<li><a rel=prefetch aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact">Contact Eddie</a></li>
		<h2>484-680-0377</h2>
	<img alt='phone icon' src='settings_phone-24px.svg' />
	</ul>
	
</nav>
