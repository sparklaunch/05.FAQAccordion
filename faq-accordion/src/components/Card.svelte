<script lang="ts">
    import Illustration from "./Illustration.svelte";
    import FAQ from "./FAQ.svelte";
</script>

<div id="card">
    <div id="left">
        <Illustration />
    </div>
    <div id="right">
        <FAQ />
    </div>
</div>

<style>
    #card {
        background-color: white;
        box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
        display: flex;
        width: 800px;
    }
    #left {
        width: 50%;
    }
    #right {
        width: 50%;
    }
</style>
