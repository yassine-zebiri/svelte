<script>
	import { Router, Link, Route } from "svelte-navigator";
  import Home from './router/home.svelte';
  import About from './router/about.svelte';
  import Blog from './router/blog.svelte';
  import LogIn from "./router/log-in.svelte";


  import './css/bootstrap-5.css';
import Header from "./lib/Header.svelte";
import Lading from "./lib/lading.svelte";
import User from "./router/user.svelte";
let lading=true;
setTimeout(()=>{
    lading=false;
},1000)

</script>
{#if lading}
<div style="margin-top:35vh" class="text-center">
  <h1>YASSINE ZEBIRI</h1>
  <Lading />
</div>
{:else}

<Router>
  <div class="contant">
  <Header/>
  <Route path={'/'}><Home/></Route>
  <Route path={'/about'}><About/></Route>
  <Route path={'/blog/*'}>
    <Route path="/">
        <Blog/>
    </Route>
    <Route path="/:id/:fname/:lname/:email/:password">
      <User/>
    </Route>

  </Route>
  <Route path={'/log-in'}><LogIn/></Route>
  </div>
</Router>
{/if}


<style>

.contant{
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>
