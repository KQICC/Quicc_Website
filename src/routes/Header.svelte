<script lang=ts>
	import './styles.css';

	function handleSectionClick(event: Event) {
		event.preventDefault();
		try {
			const link = event.currentTarget as HTMLAnchorElement;
			const anchorId = new URL(link.href).hash.slice(1);
			const anchor = document.getElementById(anchorId);
			if (anchorId === "home") {
				scrollTo({ top: 0, behavior: "smooth" });
			} else {
				scrollTo({ top: anchor.offsetTop - 50, behavior: "smooth" });
			}
		} catch (error) {
			console.error(error);	
		}
	}
</script>

<header>
	<nav>
		<ul>
			<li>
				<a href="#home" on:click={handleSectionClick}>Home</a>
			</li>
			<li>
				<a href="#about" on:click={handleSectionClick}>About</a>
			</li>
			<li>
				<a href="#members" on:click={handleSectionClick}>Members</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		justify-content: space-between;
		position: sticky;
		top: 0;
		z-index: 100; 
		/* todo change bg color */
		background: var(--color-logo-bg); 
	}

	nav {
		justify-content: center;
		--background: rgba(255, 255, 255, 1);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--color-logo-bg);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	/* !todo -> fix this */
	/* li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	} */

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-logo-primary);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-logo-tertiary);
	}
</style>
