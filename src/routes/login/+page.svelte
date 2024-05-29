<script lang="ts" >
    import { goto } from '$app/navigation';
    import { onMount } from 'svelte';
    import { user } from '../../stores/user';
    let sigin=true;
    let Email="";
    let Password="";
    let loading=false;
    let message="";
    let remember=true;

    onMount(()=>{
        let ee=localStorage.getItem('login');
        if(ee){
            goto('/home');
        }
      })

     function done(){
        if(Email.length==0 || Password.length==0){
            message="Can't Leave the Fields empty"
            return;
        }
        loading=true;
        try{
        if(sigin) {
            siginfun();
        }
        else{
              sigupfun();
        }
        }
        catch (err) {
        console.log(err);
        message="Something went wrong";
        }
    }
    async function  siginfun() {
        try{
        let a =await  fetch("http://localhost:3000/login",{
            method:"POST",
            headers:{
                "Content-Type":"application/json"
            },
            body:JSON.stringify({email:Email,signin:true,password:Password,remember:true})
        }) 
        let aa=await a.json();
        if(aa.found){
          if(remember){
          localStorage.setItem('login','true');}
          localStorage.setItem('email',Email);
          $user={email:Email};
          goto("/home"); 
          message="found";
        }
        else{
            message=aa.msg;
        }
        }
        catch (err){
            message="Something went wrong";
        }
        loading=false;
    }

    async function sigupfun() {
        try{
        let a =await  fetch("http://localhost:3000/login",{
            method:"POST",
            headers:{
                "Content-Type":"application/json"
            },
            body:JSON.stringify({email:Email,signin:false,password:Password,remember:true})
        }) 
        let aa=await a.json();
        if(!(aa.found)){
          if(remember){
          localStorage.setItem('login','true');}
          localStorage.setItem('email',Email);
          $user={email:Email};
          goto("/home"); 
          message="found";
        }
        else{
            message=aa.msg;
        }
        }
        catch (err){
            message="Something went wrong";
        }
        loading=false;
    }

</script>



<h2 class="  text-black w-max fixed top-5 left-10 font-semibold underline-offset-8 border-black border-2 px-3 decoration-black decoration-solid font-[Poppins] text-2xl " >LOOKS</h2>






<div class="flex flex-col items-center " >
<h1 class="font-[Poppins] w-full text-center my-5 mt-10 font-medium text-base " >{ sigin ? "Login to your Account" : "Create new Account" }</h1>
<div class="w-[90%]" >
<h6 class="font-[Poppins] font-medium text-xs text-[#6d6d6d] mt-3" >Email</h6>
<input bind:value={Email} class="h-10 w-full border-b-2 px-3 font-[Poppins] text-base" ></div><div class="w-[90%]" >
<h6 class="font-[Poppins] font-medium text-xs text-[#6d6d6d] mt-3" >Password</h6>
<input bind:value={Password} class="h-10 w-full border-b-2 px-3 font-[Poppins] text-base" ></div>
<div class="my-5 w-[90%] flex items-center" ><input bind:checked={remember} type="checkbox" class="mr-2 "  ><span class="font-[Poppins] text-xs" >Remember me</span></div>
{#if message}
<div  class="font-[Poppins] my-3 text-xs text-red-500" >{message}</div>{/if}
<button on:click={()=>{sigin=!sigin;Email="",Password=""}} class="font-[Poppins] my-3 text-xs " >{sigin ? "Don't have an account Create account →" : "Already a user , Log in →"}</button>
<button on:click={done} class="h-[8vh] my-2 mb-7 bg-black rounded-2xl font-semibold w-[90%] font-[Poppins] text-white" >
    {#if loading}
    <div class="loder" ></div>
    {:else}
    { sigin ? "Sign in " :"Sigin up" } 
    {/if} </button>
</div>











<style lang="postcss" >
input {
    outline: none;
}
input[type="checkbox"] {
            accent-color: black;
}
.loder{
    height: 30px;
    width: 30px;
    border:solid white  3px;
    background-color:transparent;
    border-top: solid black 3px;
    border-right: solid black 3px;
    border-radius: 50%;
    animation: ro 1s linear  infinite ;
    margin-left: auto;
    margin-right: auto;
}
@keyframes ro{
    0%{
        transform: rotate(0deg);
    }
    100%{
        transform: rotate(360deg);
    }
}
</style>


   