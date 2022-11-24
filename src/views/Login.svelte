<script>
    import {user} from '../stores/User'
    import {navigate} from 'svelte-routing'

    let email = ''
    let password = ''

    const procesarFormulario = () =>{

        //if(!email.trim() || !password.trim()){
            //console.log('Campos Vacios')
           // alert("campos vacios")
           // return
       // }
       if(!email.trim() & !password.trim()){
           alert("Email y Password vacio")
       }else if(!password.trim()){
           alert("Password vacio")
       }else if(!email.trim()){
           alert("Email vacios")
       }        
        user.setUser({
            email, password
        })

        navigate('/perfil', {replace: true})
    }
</script>

<div>
    <h1>Acceso</h1>
    <form on:submit|preventDefault={procesarFormulario}>
        <input type="text" placeholder="Ingrese Email" bind:value={email}>
        <input type="text" placeholder="Ingrese Contraseña" bind:value={password}>
        <button type="submit">Acceder</button>
    </form>
</div>