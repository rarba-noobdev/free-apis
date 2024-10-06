<script>

    export let name = "";
    console.log(name);
    


    import { resources } from "./resources";
    import { categories } from "./categories";   
</script>

<div class="container">
    <div class="api-catalog" role="region" aria-labelledby="api-categories">
        <h1 id="api-categories" class="visually-hidden">API Categories</h1>
        
            <section class="category-section">
                <h2 class="category-title">{name}</h2>
                <div class="card-grid">
                    {#each resources.entries.filter((ele) => ele.Category === name) as resource}
                        <a style="text-decoration: none;" href={resource.Link} class="card" aria-labelledby={`${resource.API}-title`}>
                            <div class="card-header">
                                <h3 id={`${resource.API}-title`} class="card-title">{resource.API}</h3>
                                <div class="status-badges">
                                    <span class="badge auth-badge" class:open={resource.Auth === ""}>
                                        {resource.Auth === "" ? "Open" : resource.Auth}
                                    </span>
                                    <span class="badge" class:available={resource.HTTPS}>HTTPS</span>
                                    <span class="badge" class:available={resource.Cors === "yes"}>CORS</span>
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
        color: #E5E7EB;
        margin-bottom: 1.5rem;
        padding-bottom: 0.5rem;
        border-bottom: 1px solid #374151;
    }

    /* Card Grid */
    .card-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 1.5rem;
    }

    /* Card Styles */
    .card {
        background-color: #1F2937;
        border: 1px solid #374151;
        border-radius: 0.5rem;
        padding: 1.25rem;
        transition: transform 0.2s, box-shadow 0.2s;
    }

    .card:hover {
        transform: translateY(-2px);
        box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
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
        color: #60A5FA;
        margin: 0;
    }

    .card-description {
        font-size: 0.875rem;
        color: #9CA3AF;
        line-height: 1.5;
        margin: 0;
    }

    /* Badge Styles */
    .status-badges {
        display: flex;
        gap: 0.5rem;
        flex-wrap: wrap;
    }

    .badge {
        font-size: 0.75rem;
        padding: 0.25rem 0.5rem;
        border-radius: 0.25rem;
        background-color: #374151;
        color: #9CA3AF;
    }

    .badge.available {
        background-color: #065F46;
        color: #A7F3D0;
    }

    .auth-badge {
        background-color: #3730A3;
        color: #C7D2FE;
    }

    .auth-badge.open {
        background-color: #065F46;
        color: #A7F3D0;
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