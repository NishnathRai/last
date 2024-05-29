<script>
   import {cart} from '../../stores/cart';

</script>

<h2 class=" left-10 text-black w-max fixed -translate-y-1/2 top-[5vh] sm:left-10 font-semibold underline-offset-8 border-black border-2 px-3 decoration-black decoration-solid font-[Poppins] text-2xl " >LOOKS</h2>

<div class="h-[10vh]  w-screen fixed top-[9vh] sm:top-0 left-0 flex items-center justify-center"  >
    <svg class="h-14 px-0 py-4  rounded-l-2xl bg-[#F4F4F4]"  xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="60" height="100" viewBox="0 0 50 50">
        <path d="M 21 3 C 11.621094 3 4 10.621094 4 20 C 4 29.378906 11.621094 37 21 37 C 24.710938 37 28.140625 35.804688 30.9375 33.78125 L 44.09375 46.90625 L 46.90625 44.09375 L 33.90625 31.0625 C 36.460938 28.085938 38 24.222656 38 20 C 38 10.621094 30.378906 3 21 3 Z M 21 5 C 29.296875 5 36 11.703125 36 20 C 36 28.296875 29.296875 35 21 35 C 12.703125 35 6 28.296875 6 20 C 6 11.703125 12.703125 5 21 5 Z"></path>
        </svg>
    <input class="h-14  font-[Poppins] w-72 bg-[#F4F4F4] rounded-r-2xl" placeholder="Search" > 
</div>

<div class="h-[10vh] flex items-center justify-center fixed top-0 right-7 sm:right-10 gap-3 sm:gap-6" >
    <div class="relative flex items-center h-9 w-9" >
    <img class="h-8" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAACrUlEQVR4nO2ZO4xMURjHf1YyjalorAqVkXg0VuFViA2xGla2oGIlXhGroluFR8Go6GzhHatCRWM7q/Co2MSuhFgVjV2yEhn55H/lkp2559wZe7+IX3KSyZzv/93/yb333O+cA/+pSwnoAW4Cr4AJNft9Q30W45qdwBhQy2ijwA4cMhuopow+BQ4DFWCOWkX/PUvFnZPWDVUZ+wrsAWY1iG0DehWbDMbN41QDvgBrInRrU4PZTsGUUu+E3YlY9kn7uugJoCf1TtgjE4tpniuH3dnCuCUTh5rIcUQ5rlMgIzKxpIkcS5XDvjOF8Vkmyk3kKCuH5SqM5HvgJc+/P5DJgHJjptpk3kHMc2C+9kebm2cgKwNmk5l6tEbUvyJP8m0SP2jCQChZeR6qvytP8oMSD9Tp35gyYL/zEpJnQP3mKZqzEvfX6R9NGbBaKS8heU6q/0yeC1yT2Eru6XiXMvA2zwUi8vSq3zxFMyRxZ53+LTJhF9+c5wIReTrlxTxF86YFdVSrqMiLLRmiy+upFtRRraIsL99ilwsLJPyIHz7JU3uMaLVEtujxwgt56sizDr+LH+7JU3eM6JhEF/HDJXnqixFdkOg4fjghT7b1FMwdiXbhh93yNBgjeiLROvywXp6GY0QfJFqIHxbJ03iowDbKvqt52jUvxfparJG/xx/j8mZ3J5MNCn6MP4blzd6X4NnhNv4YjJlNk/n6PP6oxnzfki/oUfzRF1Nx3Fewx6Oxbnmzuiu4ylyFPzpiqvKk7p+PP9pD10nJSmwq58HN36YtdOWarI1ti8YrYyF7CcluxSP8MiSPmxoF7VXQFfxyNeTwtV9Bp/DL6Ywd0N/2WPfjlwPyeJmAXe+t+KUr4JTg51mIBS3DL8vl8WWjoAkHp1K1wGZep8XjUVtW+3UU9wNY5IVjWCP9OAAAAABJRU5ErkJggg==">
    <div class="h-5 w-5 top-0 right-0 rounded-full text-xs font-[Poppins] flex items-center justify-center  bg-amber-400 absolute" >{$cart.length}</div></div>
    <img class="h-9" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAAC60lEQVR4nO2YSUhVURjHfypZUWlQpkWDFOUiW1S2iCAQWphFmyaCKIMQyoigQKigaNM6hAaigsho2ESthAiSgmolDdpk0yabB0p7vNI49H9wEOPdcwfffXB/cODx3v3/z3fuO8N3PkhISEhISEhwZgRQBxwDOoAeIAW8BG4CB4DZHnzMMweBdmlT8uqQd536Cp0CYC3wFBjw0K4BlUP4VOo3Lx5PgDVhDmI00Gp10AnsA2qAcg1yElALHAe+67kfwGbLpwH4qd++6dlaaQvktQjYD3RZ/Z0DRoUxiNsy/KJgirJoxilIo+kHmtT69Z2ZOmOzeBQBW4Cv0txSLL4wb+mCjJ4Dcxz1ZiqmNYB+fV7t6FEFdCuG84rJmQ0y+OxjEBm2WlNku0+PKsVgPNa5ioutN7GJYJxSC0KDYulWbJ5ZKeEDoDBgECVqQSgEHimmFS7C0xI1Ex/2KqaTLqL7Ei0gPtQoJnNoeuajRBOIDxMV0wcXUUoip4UVMcWKycTmmfcSlREfyhWTyck8k9kh5hMfFlo7qWcyuVUj8WGbYjrrItop0UXiw2XFtMNFVKn8qFdJYK4pBfqAP8A0V3G73sAeck+zYrnhR7xK4nc5/ldKrF203o+BSZnvyaCF3HFUMdwJmhakNTeXMfwsV9/pMI6Cw1ZqMNQ9PCpmAp/U96EwDM21s02Gr4AZRM9U6z503cP12jNlqmoY48dABdEx2arWdEWRuJp/4o06MCnM9LA74F8fnerjtZ8zw6WjZ9aaWRqi92LgrbxfALOImCnWtmxO240heJr61y953tX0GhZGAmesColJ5Mb48DGFtyOWT2uQ+lUQdgO/FcRDoNpBO8+6LphzYhc5ZokK0QNKMpuyFNIKlMH2WevBrI9YYPKhE9YUafvPPC8bVMS+BIwnhqy3Chc9g5K8en2X2fFMSTXWVABXrSJ2i1qmiH1F9++8oVFrJjONelULzkuqdVKbNpc8p1QtISEhgcD8BZSX5H28QAygAAAAAElFTkSuQmCC">
    <img  class="h-9" src="https://img.icons8.com/forma-thin/48/user.png" alt="user"/>
</div>
   
<div class="w-[90vw] h-[7vh] sm:h-[10vh] border-b-2 mt-[20vh]  sm:mt-[10vh] mx-auto flex items-center overflow-x-scroll" >
<div class="h-max w-max text-sm sm:text-base flex gap-10 font-[Poppins]" ><h4>Home</h4><h4>Men</h4><h4>Women</h4><h4>Kids</h4><h4>Sports</h4><h4>Brands</h4></div>
</div>

<slot/>

<style lang="postcss" >
input {
    outline: none;
}
</style>