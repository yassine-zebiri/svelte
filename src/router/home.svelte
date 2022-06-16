<script>
import { Link } from "svelte-navigator";

    
const data=fetch("/src/assets/json/data.json")
.then(res=>res.json())


</script>

<main class="text-center">

    <h1>HOME</h1>
    {#await data}
        <h1>lading....</h1>  
    {:then res} 
        {#each res as i}
            <h5 >full Name :<Link style="text-decoration: none"  to={`/blog/${i.id}/${i.fname}/${i.lname}/${i.email}/${i.password}`}>{i.fname+" "+i.lname}</Link> </h5>
        {/each}
    {/await}

    
</main>

<style>

</style>