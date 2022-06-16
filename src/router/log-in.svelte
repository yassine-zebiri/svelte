<script>
import SignIn from "./sign-in.svelte";
import SignUp from "./sign-up.svelte";

    let state='sign-in'
</script>

<main>
<div class="w-100 text-center mt-5">
    <button class="btn btn-outline-primary m-1" on:click={()=>state="sign-in"}>sign in</button>
    <button class="btn btn-success m-1" on:click={()=>state="sign-up"} >sign up</button>
</div>
{#if state==='sign-in'}
    <SignIn/>
{:else if state==="sign-up"}
    <SignUp/>
{/if}


</main>

<style>

</style>