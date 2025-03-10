<script>
	
	import bhagat from '$lib/images/bhagat-singh-photos.webp?url';
	
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>ImageTest
		</h1>
		<h3>Direct Src:</h3>
	
	<!-- There might be an unrelated issue with importing img src=".webp" because it won't build locally with npm run build either.	However, the imported src successfully builds locally with npm run build, but won't build on cloudflare pages. So I'm commenting this out, to focus on the part that won't build on Cloudflare pages, and troubleshoot this part later on.
	 
	<img src="./src/lib/images/bhagat-singh-photos.webp" alt="Bhagat" type="image/webp" /> 
	-->
	 
	<h3>Imported Src:</h3>
<img src={bhagat} alt="Bhagat" type="image/webp" /> 
	</section>

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
