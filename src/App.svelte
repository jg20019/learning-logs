<script>
import Home from './lib/Home.svelte';
import Layout from './lib/Layout.svelte';
import TopicDetail from './lib/TopicDetail.svelte';

let topicName = 'Learning C#'
let topics = [
    { 
      name: 'Learning C#',
      entries: [
        {date: '2023-05-01', minutes: 85,  desc: 'Introduction to C#'},
        {date: '2023-05-02', minutes: 90,  desc: 'Making a CLI'},
        {date: '2023-05-03', minutes: 120, desc: 'Making Quick Block'},
        {date: '2023-05-12', minutes: 30,  desc: 'DNS in a Weekend'},
        {date: '2023-05-13', minutes: 45,  desc: 'DNS in a Weekend'},
        {date: '2023-05-13', minutes: 30,  desc: 'DNS in a Weekend'},
        {date: '2023-05-14', minutes: 45,  desc: 'DNS in a Weekend'},
      ]
    }
]

$: currentTopic = topics.find(({name}) => topicName === name)

</script>

<main>
    <Layout on:go-home={() => topicName = null }> 
        {#if topicName === null }
            <Home /> 
        {:else}
            <TopicDetail topic={currentTopic} />
        {/if}
    </Layout>
</main>

<style>
</style>
