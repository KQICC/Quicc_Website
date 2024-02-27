<script>
	// import welcome from '$lib/images/svelte-welcome.webp';
	import logo from '$lib/images/logo-nobg.png';
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<!-- Home section -->
<section id="home">
	<h1> Kharagpur Quantum Information and Computing Club </h1>
	<!-- Logo -->
	<img src={logo} id="logo" alt="KQICC logo" />
</section>

<!-- About section -->
<section id="about">
<div class="text-column">
	<h1>About Us</h1>

	<p>
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo inventore itaque voluptatum accusantium? Sapiente incidunt dolore nobis atque aperiam! Nulla quos tenetur id officia doloremque rerum minus odit tempora excepturi possimus minima maxime nobis, eius cum earum debitis inventore dolor.
	</p>

	<p>
		Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure architecto maxime quae modi at reiciendis animi, eos quam non debitis a repellat ad culpa, cumque accusantium. Modi error eaque ea!
	</p>

	<p>
		Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti nobis explicabo porro dolor tempora quos quo quia, ea officia.
	</p>
</div>
</section>

<!-- Members section -->
<section id="members">
	<div class="text-column">
		<h1>Members</h1>
	
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo inventore itaque voluptatum accusantium? Sapiente incidunt dolore nobis atque aperiam! Nulla quos tenetur id officia doloremque rerum minus odit tempora excepturi possimus minima maxime nobis, eius cum earum debitis inventore dolor.
		</p>
	
		<p>
			Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure architecto maxime quae modi at reiciendis animi, eos quam non debitis a repellat ad culpa, cumque accusantium. Modi error eaque ea!
		</p>
	
		<p>
			Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti nobis explicabo porro dolor tempora quos quo quia, ea officia.
		</p>
	</div>
</section>


<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	section h1 {
		font-size: 2rem;
		text-align: center;
		margin-bottom: 0rem;
		color: var(--color-logo-secondary);
	}

	#logo {
		width: 70%;
		height: auto;
	}
</style>
