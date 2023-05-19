<script>
import { createEventDispatcher } from 'svelte'

const dispatch = createEventDispatcher();

function goHome() {
    dispatch('go-home');
}
</script>

<div class="container w-10/12 mx-auto">
    <header class="mb-10 border-black border-b py-5 flex justify-between">
        <h1 class="font-bold text-2xl cursor-pointer"> Study Log </h1>
        <button 
            on:click={goHome} 
            class="bg-green-500 p-2 text-white rounded font-bold 
                   hover:bg-green-700"> 
            Go back 
        </button>
    </header>
    <slot></slot>
</div>
