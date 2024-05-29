<script lang="ts" >
    import { goto } from '$app/navigation';
</script>


<div class="h-max w-screen bg-[#f4f4f4]  flex-col-reverse sm:flex-row flex" > 

    <div class='sm:h-[90vh] mt-5 sm:pt-20 sm:my-[5vh] sm:w-1/2 flex items-center flex-col justify-between' >
    <div class='h-max sm:h-[65%] flex items-center flex-col justify-center bg-transparent w-[90%]' >
    <div class=' flex my-4 sm:my-0 items-center flex-col justify-center bg-transparent w-full' >
        <h1 class="text-base text-black sm:mb-5  font-[Poppins]" >LARGEST BRAND COLLECTIONS</h1>
        <h1 class=" text-black  font-semibold leading-relaxed sm:leading-none	my-3 text-center  text-5xl font-[Poppins]" ><spane class=" border-2 px-3 decoration-[#4b7416] shadow-xl decoration-solid " >AI</spane> PICK STYLES</h1>
        <h1 class=" text-black font-semibold mb-5 sm:my-5  text-5xl font-[Poppins]" > JUST FOR YOU</h1>
    </div>
    <button on:click={()=>{goto('/home')}} class="cursor-pointer font-[Poppins] text-base mt-5 sm:mt-11 mb-10  underline-offset-8 underline" >Skip  sign in→ </button>
    </div>

    <div class="sm:rounded-2xl items-center justify-center py-10 h-max flex-col sm:flex-row px-10  sm:px-24 sm:h-[30%] w-[100%] sm:w-[90%] bg-center bg-cover flex  bg-[url('https://images.unsplash.com/photo-1497997092403-f091fcf5b6c4?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')]" >
        <h2 class="text-base text-white mb-5 mr-10  font-semibold font-[Poppins]" >About</h2>
        <h3 class="text-sm text-[#d4d4d4]  font-[Poppins]" >"We have a great collection of all popular brand items. Our<span class="text-base pl-1 text-white  font-[Poppins]" > AI now selects the best clothes for you</span> , ensuring a perfect fit and style every time."</h3>
    </div>
    </div>
    
    <div class='h-[100vh] sm:h-[90vh] sm:my-[5vh] w-full sm:w-1/2 flex items-center justify-center' >
    <div class="w-[100%] sm:mr-10 h-full bg-center bg-cover sm:rounded-2xl bg-[url('https://images.unsplash.com/photo-1544441893-675973e31985?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')] flex items-center flex-col justify-center" >
        <h2 class="text-white font-semibold underline-offset-8 border-2 px-3 decoration-white decoration-solid font-[Poppins] text-2xl " >LOOKS</h2>
        <h4 class="text-white pb-10 pt-2 font-[Poppins] text-sm " >Elevate Your Wardrobe</h4>
        <div class="h-max w-[90%] sm:w-[60%] bg-white rounded-2xl" >
         <slot/>
        </div>
    </div>
    </div>
    
    </div>
    
    
    






    <style lang="postcss" >
    </style>
    
    