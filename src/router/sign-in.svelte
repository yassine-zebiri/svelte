<script>
    let data={
        email:'',
        password:''
    }
    
    </script>
    
    <main>
        <div class="form mt-5">
            <div class="text-center">
                <h3>sign in</h3>
            </div>
        <div class="form-floating mb-3 mt-5">
        
        <input placeholder="email" class="form-control" id="email" type="email" bind:value={data.email} name="email">
        <label for="email">email</label>
    
        </div>
    
        <div class="form-floating mb-3 mt-3">
    
        
        <input class="form-control" placeholder="password" bind:value={data.password} name="password" id="password">
        <label for="password">password</label>
    </div>
        <button class="btn btn-primary w-100 mt-3 mb-5" on:click={()=>alert(JSON.stringify (data) )} >sign in</button>
        </div>
    </main>
    
    <style>
    .form{
        width: 500px;
        padding: 1rem;
        border: 1px rgba(143, 143, 143, 0.303) solid;
        margin: auto;
        border-radius: 1rem;
    }
    
    </style>