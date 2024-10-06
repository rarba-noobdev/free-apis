<script>
	import AllApis from "./all-apis.svelte";
	import Categories from "./categories.svelte";
	import Specific from "./specific.svelte";

</script>
<AllApis></AllApis>
<!-- <Specific name="Anime"></Specific> -->
<!-- <Categories></Categories> -->

<!-- <header>
	<h2>/\\/</h2>
	<a style="font-family: Clash Display;" href="" class="browse-link">Browse All</a>
	<div class="github-link">
	  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 16 16" fill="currentColor">
		<path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8"/>
	  </svg>
	</div>
  </header>

  <p style="text-align:center; font-family: Clash Display;">Discover a curated selection of public APIs sourced from <a href="https://github.com/marcelscruz/public-apis">public-apis</a>, created by <a href="https://github.com/marcelscruz">marcelscruz</a>.</p>

  

  <main>
	<h1>Discover Your Options</h1>
	<div class="link-cards">
	  <div>
		<a href="https://github.com/marcelscruz/public-apis/blob/main/db/resources.json">Browse API Categories</a>
<p>Unlock a vast collection of public APIs, thoughtfully categorized to suit your needs—whether you're exploring Finance, Business, Health, or Science. Elevate your next project by finding the perfect API from our diverse library.</p>


	  </div>
	  <div>
		<a href="https://github.com/marcelscruz/public-apis/blob/main/db/resources.json">View All APIs</a>
		<p>Unlock the full potential of our API treasure trove! Explore a variety of categories—whether you need data, entertainment, or innovative tools, we’ve got everything to fuel your next project. Click above to dive into the complete collection!</p>
	  </div>	  
	</div>
  </main>
  <footer>
	<p style="font-family: Clash Display;">
		Developed by 
		<a  href="https://www.instagram.com/rarbanoobdev_/" target="_blank" rel="noopener noreferrer">rarbanoobdev_</a>
	</p>
	
</footer>
  <style>

footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%; /* Ensures the footer takes the full width */
    text-align: center; /* Center align the text */
}

	header {
		display: grid;
		text-align: center;
		align-items: center;
		grid-template-columns: 1fr 1fr 1fr;

	}
  
	h1 {
	  font-size: 2rem;
	  font-weight: 400;
	  margin: 2rem 0;
	}
  
	.browse-link {
	  color: #7dd3fc;
	}
  
	.github-link {
	  color: #94a3b8;
	}
  
	.link-cards {
	  display: flex;
	  gap: 1rem;

	}
  
	.link-cards div {
	  padding: 1rem 2rem;
	  /* background-color: #222831; */
	  background: linear-gradient(to bottom, rgba(255,255,255,0.15) 0%, rgba(0,0,0,0.15) 100%), radial-gradient(at top center, rgba(255,255,255,0.40) 0%, rgba(0,0,0,0.40) 120%) #989898;
	  background-blend-mode: multiply,multiply;	  width: 25vw;
	  border-radius: 0.5rem;
	  box-shadow: 0 1px 3px rgba(46, 18, 18, 0.1);
	  
	}
	.link-cards div a {
		font-size: 1.5rem;
	}
  
	main {
	  padding: 0 1rem;
	}
  </style> -->