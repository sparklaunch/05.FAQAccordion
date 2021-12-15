<script lang="ts">
    import Card from "./components/Card.svelte";
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
        href="https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap"
        rel="stylesheet"
    />
</svelte:head>
<div id="app">
    <Card />
</div>

<style>
    #app {
        width: 100vw;
        height: 100vh;
        background: linear-gradient(rgb(166, 93, 231), rgb(90, 88, 229));
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
