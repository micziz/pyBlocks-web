<script>
    import Router from 'svelte-spa-router'
    import Home from "./routes/Home.svelte";
    import Contributing from "./routes/Contributing.svelte";
    import NotFound from "./routes/NotFound.svelte";
    const routes = {
      '/': Home,
  
      '/contributing': Contributing,
  
      '*': NotFound,
    }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;500;600;700&family=Open+Sans:wght@300&family=PT+Sans&display=swap');

  #navbar{
    display: flex;
    justify-content: center;
    align-items: center;
  }

  #home{
    font-family: 'Hind Siliguri', sans-serif;
    margin-top: 10px;
    margin-right: 10px;
  }

  #contributing{
    font-family: 'Hind Siliguri', sans-serif;
    margin-top: 10px;
    margin-right: 10px;
  }
</style>


<nav id=navbar>
  <a href="/#/" id="home">Home</a>
  <a href="/#/contributing" id="contributing">Contributing</a>
</nav>


<body>  
  <Router {routes}/>
</body>