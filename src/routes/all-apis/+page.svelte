<script>
    import { resources } from "../resources";
    import { categories } from "../categories";   
</script>

<svelte:head>
    <title>All Apis - Free APIs Collection</title>
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

<header class="all-apis-header">
    <h1 class="all-apis-title" aria-level="1">All APIs</h1>
    <div class="all-apis-nav-links">
        <a href="./" rel="noopener noreferrer" class="all-apis-nav-link">Home</a>
        <a href="./categories" rel="noopener noreferrer" class="all-apis-nav-link">All Categories</a>
    </div>
</header>

<hr class="all-apis-divider">

<div class="all-apis-container">
    <div class="all-apis-catalog" role="region" aria-labelledby="all-apis-categories">
        <h1 id="all-apis-categories" class="all-apis-visually-hidden">API Categories</h1>
        {#each categories.entries as category}
            <section class="all-apis-category-section">
                <h2 class="all-apis-category-title">{category.name}</h2>
                <div class="all-apis-card-grid">
                    {#each resources.entries.filter((ele) => ele.Category === category.name) as resource}
                    <a target="_blank" href={resource.Link} class="all-apis-card" aria-labelledby={`${resource.API}-title`}>
                        <div class="all-apis-card-header">
                            <h3 id={`${resource.API}-title`} class="all-apis-card-title">{resource.API}</h3>
                            <div class="all-apis-status-badges">
                                <span class="all-apis-badge all-apis-auth-badge" class:open={resource.Auth === ""}>
                                    {resource.Auth === "" ? "Open" : resource.Auth}
                                </span>
                                <span class="all-apis-badge" class:available={resource.HTTPS}>HTTPS</span>
                                <span class="all-apis-badge" class:available={resource.Cors === "yes"}>CORS</span>
                            </div>
                        </div>
                        <p class="all-apis-card-description">{resource.Description}</p>
                    </a>
                    {/each}
                </div>
            </section>
        {/each}
    </div>
</div>

<style>
    /* Container and Global Styles */
    .all-apis-container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem;
    }

    /* Header Styles */
    .all-apis-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .all-apis-title {
        font-size: 1.5rem;
        font-weight: 600;
        color: #E5E7EB;
        margin-bottom: 1.5rem;
        padding-bottom: 0.5rem;
    }

    .all-apis-nav-links {
        display: flex;
        gap: 1rem;
    }

    .all-apis-nav-link {
        color: #7DD3FC;
        text-decoration: none;
        transition: color 0.2s;
    }

    .all-apis-nav-link:hover {
        color: #3B82F6;
    }

    /* Divider Styles */
    .all-apis-divider {
        border-bottom: 1px solid #374151;
        margin-top: -10px;
    }

    /* Category Styles */
    .all-apis-category-section {
        margin-bottom: 3rem;
    }

    .all-apis-category-title {
        font-size: 1.5rem;
        font-weight: 600;
        color: #E5E7EB;
        margin-bottom: 1.5rem;
        padding-bottom: 0.5rem;
        border-bottom: 1px solid #374151;
    }

    /* Card Grid */
    .all-apis-card-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 1.5rem;
    }

    /* Card Styles */
    .all-apis-card {
        background-color: #1F2937;
        border: 1px solid #374151;
        border-radius: 0.5rem;
        padding: 1.25rem;
        transition: transform 0.2s, box-shadow 0.2s;
        text-decoration: none;
    }

    .all-apis-card:hover {
        transform: translateY(-2px);
        box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    }

    .all-apis-card-header {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        margin-bottom: 1rem;
    }

    .all-apis-card-title {
        font-size: 1.125rem;
        font-weight: 600;
        color: #60A5FA;
        margin: 0;
    }

    .all-apis-card-description {
        font-size: 0.875rem;
        color: #9CA3AF;
        line-height: 1.5;
        margin: 0;
    }

    /* Badge Styles */
    .all-apis-status-badges {
        display: flex;
        gap: 0.5rem;
        flex-wrap: wrap;
    }

    .all-apis-badge {
        font-size: 0.75rem;
        padding: 0.25rem 0.5rem;
        border-radius: 0.25rem;
        background-color: #374151;
        color: #9CA3AF;
    }

    .all-apis-badge.available {
        background-color: #065F46;
        color: #A7F3D0;
    }

    .all-apis-auth-badge {
        background-color: #3730A3;
        color: #C7D2FE;
    }

    .all-apis-auth-badge.open {
        background-color: #065F46;
        color: #A7F3D0;
    }

    /* Accessibility */
    .all-apis-visually-hidden {
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
        .all-apis-container {
            padding: 1rem;
        }

        .all-apis-card-grid {
            grid-template-columns: 1fr;
        }

        .all-apis-category-title {
            font-size: 1.25rem;
        }
    }
</style>
