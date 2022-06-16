<script>
	import { useParams } from "svelte-navigator";

	const params = useParams();

	$: console.log($params); // -> { id: "123", splat: "pauls-profile" }
</script>
<main class="mt-5 border p-3">
    <h5>id :{$params.id}</h5>
    <h5>first Name : {$params.fname}</h5>
    <h5>last Name : {$params.lname}</h5>
    <h5>email : {$params.email}</h5>
    <h5>password : {$params.password}</h5>
</main>