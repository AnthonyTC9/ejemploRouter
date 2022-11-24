<script>
    import {Link, navigate} from 'svelte-routing'
    import {user} from "../stores/User"

    const cerrarSesion = () =>{
        user.setUser(null)
        navigate('/login', {replace:true})
    }
</script>

<nav>
    {#if $user}
         <Link to="/perfil">PERFIL</Link>
         <button on:click={cerrarSesion}>Cerrar Sesiòn</button>
    {:else}
         <Link to="/">HOME</Link>
         <Link to="/about">ABOUT</Link>
         <Link to="/login">LOGIN</Link>
    {/if}
</nav>