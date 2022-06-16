<script>
    const data={
        fname:'',
        lname:'',
        email:'',
        password:''
    }
</script>
<main>
    <div class="row g-3 sign-up mt-5">
        <div class="text-center">
            <h3>sign up</h3>
        </div>
        <div class="col-md-6">
            <label for="" class="form-label">first name</label>
            <input type="text" class="form-control" bind:value={data.fname}>
        </div>
        <div  class="col-md-6">
            <label for="" class="form-label" >last name</label>
            <input type="text" class="form-control"  bind:value={data.lname}>
        </div>
        <div  class="col-md-12">
            <label for="" class="form-label" >email</label>
            <input type="email" class="form-control"  bind:value={data.email}>
        </div>
        <div  class="col-md-12">
            <label for="" class="form-label" >password</label>
            <input type="password" class="form-control"  bind:value={data.password}>
        </div>
        <button on:click={()=>alert(JSON.stringify (data) )} class="w-100 btn btn-primary w-100 mt-3 mb-5">sign up</button>
    </div>
</main>

<style>
.sign-up{
    width: 500px;
    padding: 1rem;
    border: 1px rgba(143, 143, 143, 0.303) solid;
    margin: auto;
    border-radius: 1rem;
}
</style>