 <script lang="ts" >
   import { goto } from '$app/navigation';
   import { onMount } from 'svelte';

   onMount(()=>{
        let ee=localStorage.getItem('login');
        if(ee){
            goto('/home');
        }
        else{
            goto('/login');
        }
  })     

</script>



<!-- <button on:click={ok} >Start</button>

// <style>

// </style> -->

<slot/>