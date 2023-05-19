<script>
    export let topic = null
</script>

{#if topic == null }
    <h1> Topic not found </h1>
{:else }
    <h1> { topic.name } </h1>
{/if}
