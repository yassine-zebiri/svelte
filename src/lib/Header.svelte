<script>
    import {Link} from "svelte-navigator";
</script>

<nav class="navbar w-h bg-primary  text-center bg-red "  >
        <Link class="nav-link bg-red text-light w-25 kad"  to={'/'}>Home</Link>
        <Link class="nav-link bg-red text-light w-25" to={'/about'}>About</Link>
        <Link class="nav-link f text-light w-25" to={'/blog'}>Blog</Link>
        <Link class="nav-link text-light w-25" to={'/log-in'}>Log in</Link>
</nav>

<style>
.w-h{
    width: 50%;
}
@media(max-width:600px){
    .w-h{
        width: 90%;
    }
}
</style>
