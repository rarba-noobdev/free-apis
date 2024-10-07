
<div class="container">
	<header class="header">
	  <h2 class="logo">/\\/</h2>
	  <nav class="nav-links">
		<a href="./all-apis" class="browse-link">Browse All</a>
		<a aria-label="github-link"
		  href="https://github.com/rarba-noobdev/free-apis"
		  class="github-link"
		  target="_blank"
		  rel="noopener noreferrer"
		>
		  <svg 
			xmlns="http://www.w3.org/2000/svg" 
			width="20" 
			height="20" 
			viewBox="0 0 16 16" 
			fill="currentColor"
		  >
			<path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8"/>
		  </svg>
		</a>
	  </nav>
	</header>
  
	<p class="intro-text">
	  Discover a curated selection of public APIs sourced from 
	  <a 
		href="https://github.com/marcelscruz/public-apis" 
		target="_blank" 
		rel="noopener noreferrer"
	  >public-apis</a>, 
	  created by 
	  <a 
		href="https://github.com/marcelscruz" 
		target="_blank" 
		rel="noopener noreferrer"
	  >marcelscruz</a>.
	</p>
  
	<main class="main">
	  <h1 class="main-title">Discover Your Options</h1>
	  <div class="link-cards">
		<div class="card">
		  <a href="./categories" class="category-link">Browse API Categories</a>
		  <p class="card-text">
			Unlock a vast collection of public APIs, thoughtfully categorized to suit your needs—whether you're exploring Finance, Business, Health, or Science. Elevate your next project by finding the perfect API from our diverse library.
		  </p>
		</div>
		<div class="card">
		  <a 
			href="./all-apis" 
			rel="noopener noreferrer"
			class="all-apis-link"
		  >
			View All APIs
		  </a>
		  <p class="card-text">
			Unlock the full potential of our API treasure trove! Explore a variety of categories—whether you need data, entertainment, or innovative tools, we've got everything to fuel your next project. Click above to dive into the complete collection!
		  </p>
		</div>
	  </div>
	</main>
  
	<footer class="footer">
	  <p>
		Developed by 
		<a 
		  href="https://www.instagram.com/rarbanoobdev_/" 
		  target="_blank" 
		  rel="noopener noreferrer"
		  class="footer-link"
		>rarbanoobdev_</a>
	  </p>
	</footer>
  </div>
  
  <style>
	.container {
	  background-color: #0f172a;
	  color: #e2e8f0;
	  line-height: 1.5;
	  min-height: 100vh;
	  display: flex;
	  flex-direction: column;
	  margin: 0;
	 }
  
	.header {
	  display: flex;
	  justify-content: space-between;
	  align-items: center;
	  padding: 1.5rem 2rem;
	  max-width: 1200px;
	  margin: 0 auto;
	  width: 100%;
	}
  
	.logo {
	  font-size: 1.5rem;
	  font-weight: 600;
	  color: #7dd3fc;
	  margin: 0;
	}
  
	.nav-links {
	  display: flex;
	  gap: 1.5rem;
	  align-items: center;
	}
  
	.browse-link {
	  color: #7dd3fc;
	  text-decoration: none;
	  transition: color 0.2s;
	}
  
	.browse-link:hover {
	  color: #3b82f6;
	}
  
	.github-link {
	  color: #e2e8f0;
	  transition: color 0.2s;
	}
  
	.github-link:hover {
	  color: #7dd3fc;
	}
  
	.intro-text {
	  text-align: center;
	  max-width: 800px;
	  margin: 2rem auto;
	  padding: 0 2rem;
	}
  
	.intro-text a {
	  color: #7dd3fc;
	  text-decoration: none;
	  transition: color 0.2s;
	}
  
	.intro-text a:hover {
	  color: #3b82f6;
	}
  
	.main {
	  flex-grow: 1;
	  padding: 2rem;
	  max-width: 1200px;
	  margin: 0 auto;
	  width: 100%;
	}
  
	.main-title {
	  font-size: 2.5rem;
	  font-weight: 600;
	  margin-bottom: 2rem;
	  text-align: center;
	  color: #7dd3fc;
	}
  
	.link-cards {
	  display: grid;
	  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
	  gap: 2rem;
	}
  
	.card {
	  background: #1e293b;
	  border-radius: 0.75rem;
	  padding: 2rem;
	  transition: transform 0.3s, box-shadow 0.3s;
	  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
	}
  
	.card:hover {
	  transform: translateY(-5px);
	  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
	}
  
	.card a {
	  font-size: 1.5rem;
	  color: #7dd3fc;
	  text-decoration: none;
	  display: block;
	  margin-bottom: 1rem;
	  transition: color 0.2s;
	}
  
	.card a:hover {
	  color: #3b82f6;
	}
  
	.card-text {
	  color: #94a3b8;
	  margin: 0;
	}
  
	.footer {
	  padding: 2rem;
	  text-align: center;
	  background-color: #1e293b;
	  margin-top: auto;
	}
  
	.footer-link {
	  color: #7dd3fc;
	  text-decoration: none;
	  transition: color 0.2s;
	}
  
	.footer-link:hover {
	  color: #3b82f6;
	}
  
	@media (max-width: 768px) {
	  .header {
		flex-direction: column;
		gap: 1rem;
		text-align: center;
	  }
  
	  .nav-links {
		justify-content: center;
	  }
  
	  .main-title {
		font-size: 2rem;
	  }
  
	  .link-cards {
		grid-template-columns: 1fr;
	  }
	}
  </style>
  