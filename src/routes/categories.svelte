<script>
    import { categories } from "./categories";  
</script>

<h1 style="        font-size: 1.5rem;
        font-weight: 600;
        color: #E5E7EB;
        margin-bottom: 1.5rem;
        padding-bottom: 0.5rem;
        border-bottom: 1px solid #374151;;" aria-level="1">Categories</h1>

<div class="categories-container"> 
    {#each categories.entries as category}
        
    <button style=" font-size: 1.125rem;
        font-weight: 600;
        color: #60A5FA;
        margin: 0;" class="category">
            {category.name}
        </button>
    {/each}
</div>

<style>
    .categories-container {
        display: grid;
        grid-template-columns: repeat(7,1fr);
        gap: 1rem; /* Changed to rem for consistency */
    }

    .category {
        background-color: #1F2937;
        border: 1px solid #374151;
        border-radius: 0.5rem;
        padding: 1.25rem;
        transition: transform 0.2s, box-shadow 0.2s;
    }

    .category:hover {
        transform: translateY(-2px);
        box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    }
</style>
