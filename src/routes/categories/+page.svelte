<script>
    import { categories } from "../categories";  
</script>
<svelte:head>
    <title>Categories - Free APIs Collection</title>
<meta name="description" content="Discover a curated collection of free public APIs across various categories. Enhance your applications with easy access to weather, finance, and other essential data.">
<meta name="keywords" content="free APIs, public APIs, API collection, weather API, finance API, social media APIs, entertainment APIs, sports APIs, data integration, RESTful APIs, open-source APIs, developer resources, programming, software development, technology, application programming interfaces, JSON APIs">
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://free-apis-zeta.vercel.app/">
<meta property="og:title" content="Free APIs Collection">
<meta property="og:description" content="Explore a wide range of free public APIs for your development projects. Find APIs for weather, finance, and more.">
<meta property="og:url" content="https://free-apis-zeta.vercel.app/">
<meta property="og:type" content="website">
<meta name="author" content="Free APIs Team">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#ffffff">
<meta property="og:site_name" content="Free APIs">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Free APIs Collection">
<meta name="twitter:description" content="Find a variety of free public APIs for your development needs, from weather data to finance information.">
<meta name="twitter:url" content="https://free-apis-zeta.vercel.app/">
 

</svelte:head>
<header>
    <h1 style="font-size: 1.5rem;
        font-weight: 600;
        color: #E5E7EB;
        margin-bottom: 1.5rem;
        padding-bottom: 0.5rem;" aria-level="1">Categories</h1>

    <div class="header-links">
        <a href="./" class="header-link">Home</a>
        <a href="./all-apis" class="header-link">View All</a>
    </div>
</header>
<hr style="border-bottom: 1px solid #374151; margin-top:-10px;">

<div class="categories-container"> 
    {#each categories.entries as category}
    <a href="/categories/{category.name}" class="category">
        {category.name}
    </a>
    {/each}
</div>

<style>
    .categories-container {
        display: grid;
        grid-template-columns: repeat(6,1fr);
        gap: 1rem;
    }

    .category {
        background-color: #1F2937;
        border: 1px solid #374151;
        border-radius: 0.5rem;
        padding: 1.25rem;
        font-size: 1.125rem;
        font-weight: 600;
        color: #60A5FA;
        text-decoration: none;
        transition: transform 0.2s, box-shadow 0.2s;
    }

    .category:hover {
        transform: translateY(-2px);
        box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
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
        color: #60A5FA;
        text-decoration: none;
        font-weight: 500;
    }

    .header-link:hover {
        text-decoration: underline;
    }

    @media (max-width: 768px) {
        .categories-container {
            padding: 1rem;
            grid-template-columns: 1fr;
        }
    }
</style>