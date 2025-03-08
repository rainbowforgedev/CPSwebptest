<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import bhagat from '$lib/images/29132-8-bhagat-singh-photos.webp';
	// import welcomeFallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<picture>
				<!-- <source srcset={welcome} type="image/webp" /> -->
				 <img src={welcome} alt="Welcome" type="image/webp" /> 
				
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>

	<Counter />
</section>
<enhanced:img src="$lib/images/svelte-welcome.png" alt="Welcome" /> 
<enhanced:img src="$lib/images/29132-8-bhagat-singh-photos.png" alt="Welcome" /> 
<img src={bhagat} alt="Bhagat" type="image/webp" /> 
<style>

	img {
		width: 100%;
		height: auto;
	}
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
