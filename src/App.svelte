<script>
import Layout from './lib/Layout.svelte';
import Home from './lib/Home.svelte';

let view = 'Learning C#'


</script>

<main>
    <Layout on:go-home={() => view = 'home'}> 
        {#if view != "home" }
            <h1> { view } </h1>
        {:else}
            <Home /> 
        {/if}
    </Layout>
</main>

<style>
</style>
