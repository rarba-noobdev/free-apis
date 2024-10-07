<script>
	import { page } from '$app/stores';

	import { resources } from '../../resources';
	let name = $page.params.specific.toLowerCase();
	// console.log(name);
</script>

<svelte:head>
	<title>{name} - Free APIs Collection</title>
	<meta
		name="description"
		content="Discover a curated collection of free public APIs across various categories. Enhance your applications with easy access to weather, finance, and other essential data."
	/>
	<meta
		name="keywords"
		content="free APIs, public APIs, API collection, weather API, finance API, social media APIs, entertainment APIs, sports APIs, data integration, RESTful APIs, open-source APIs, developer resources, programming, software development, technology, application programming interfaces, JSON APIs"
	/>
	<meta name="robots" content="index, follow" />
	<link rel="canonical" href="https://free-apis-zeta.vercel.app/" />
	<meta property="og:title" content="Free APIs Collection" />
	<meta
		property="og:description"
		content="Explore a wide range of free public APIs for your development projects. Find APIs for weather, finance, and more."
	/>
	<meta property="og:url" content="https://free-apis-zeta.vercel.app/" />
	<meta property="og:type" content="website" />
	<meta name="author" content="Free APIs Team" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<meta name="theme-color" content="#ffffff" />
	<meta property="og:site_name" content="Free APIs" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Free APIs Collection" />
	<meta
		name="twitter:description"
		content="Find a variety of free public APIs for your development needs, from weather data to finance information."
	/>
	<meta name="twitter:url" content="https://free-apis-zeta.vercel.app/" />
</svelte:head>

<div class="container">
	<div class="api-catalog" role="region" aria-labelledby="api-categories">
		<h1 id="api-categories" class="visually-hidden">API Categories</h1>
		<header>
			<h2
				class="category-title"
				style="font-size: 1.5rem;
                 font-weight: 600;
                 color: #E5E7EB;
                 margin-bottom: 1.5rem;
                 padding-bottom: 0.5rem;"
				aria-level="1"
			>
				{name[0].toUpperCase() + name.slice(1)}
			</h2>

			<div class="header-links">
				<a href="./../" class="header-link">Home</a>
				<a href="./" class="header-link">Categories</a>
				<a href="./../all-apis" class="header-link">View All</a>
			</div>
		</header>
		<hr style="border-bottom: 1px solid #374151; margin-top:-10px;" />
		<section class="category-section">
			<div class="card-grid">
				{#each resources.entries.filter((ele) => ele.Category.toLowerCase() === name) as resource}
					<a
						style="text-decoration: none;"
						href={resource.Link}
						class="card"
						aria-labelledby={`${resource.API}-title`}
					>
						<div class="card-header">
							<h3 id={`${resource.API}-title`} class="card-title">{resource.API}</h3>
							<div class="status-badges">
								<span class="badge auth-badge" class:open={resource.Auth === ''}>
									{resource.Auth === '' ? 'Open' : resource.Auth}
								</span>
								<span class="badge" class:available={resource.HTTPS}>HTTPS</span>
								<span class="badge" class:available={resource.Cors === 'yes'}>CORS</span>
							</div>
						</div>
						<p class="card-description">{resource.Description}</p>
					</a>
				{/each}
			</div>
		</section>
	</div>
</div>

<style>
	/* Container and Global Styles */
	.container {
		max-width: 1200px;
		margin: 0 auto;
		padding: 2rem;
	}

	/* Category Styles */
	.category-section {
		margin-bottom: 3rem;
	}

	.category-title {
		font-size: 1.5rem;
		font-weight: 600;
		color: #e5e7eb;
		margin-bottom: 1.5rem;
		padding-bottom: 0.5rem;
		/* border-bottom: 1px solid #374151; */
	}

	/* Card Grid */
	.card-grid {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
		gap: 1.5rem;
	}

	/* Card Styles */
	.card {
		background-color: #1f2937;
		border: 1px solid #374151;
		border-radius: 0.5rem;
		padding: 1.25rem;
		transition:
			transform 0.2s,
			box-shadow 0.2s;
	}

	.card:hover {
		transform: translateY(-2px);
		box-shadow:
			0 4px 6px -1px rgba(0, 0, 0, 0.1),
			0 2px 4px -1px rgba(0, 0, 0, 0.06);
	}

	.card-header {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		margin-bottom: 1rem;
	}

	.card-title {
		font-size: 1.125rem;
		font-weight: 600;
		color: #60a5fa;
		margin: 0;
	}

	.card-description {
		font-size: 0.875rem;
		color: #9ca3af;
		line-height: 1.5;
		margin: 0;
	}

	/* Badge Styles */
	.status-badges {
		display: flex;
		gap: 0.5rem;
		flex-wrap: wrap;
	}

	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.header-links {
		display: flex;
		gap: 1rem;
	}

	.header-link {
		color: #60a5fa;
		text-decoration: none;
		font-weight: 500;
	}

	.header-link:hover {
		text-decoration: underline;
	}

	.badge {
		font-size: 0.75rem;
		padding: 0.25rem 0.5rem;
		border-radius: 0.25rem;
		background-color: #374151;
		color: #9ca3af;
	}

	.badge.available {
		background-color: #065f46;
		color: #a7f3d0;
	}

	.auth-badge {
		background-color: #3730a3;
		color: #c7d2fe;
	}

	.auth-badge.open {
		background-color: #065f46;
		color: #a7f3d0;
	}

	/* Accessibility */
	.visually-hidden {
		position: absolute;
		width: 1px;
		height: 1px;
		padding: 0;
		margin: -1px;
		overflow: hidden;
		clip: rect(0, 0, 0, 0);
		white-space: nowrap;
		border: 0;
	}

	/* Responsive Design */
	@media (max-width: 768px) {
		.container {
			padding: 1rem;
		}

		.card-grid {
			grid-template-columns: 1fr;
		}

		.category-title {
			font-size: 1.25rem;
		}
	}
</style>
