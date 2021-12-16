<script lang="ts">
    import Illustration from "./Illustration.svelte";
    import FAQ from "./FAQ.svelte";
    export let data;
</script>

<div id="card-wrapper">
    <div id="card">
        <div id="left">
            <Illustration />
        </div>
        <div id="right">
            <FAQ {data} />
        </div>
    </div>
    <img src="/assets/illustration-box-desktop.svg" alt="Box" />
</div>

<style>
    #card-wrapper {
        position: relative;
    }
    #card-wrapper > img {
        position: absolute;
        top: 20vh;
        left: -12vh;
    }
    #card {
        background-color: white;
        box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
        display: flex;
        width: 800px;
        overflow: hidden;
        height: 550px;
    }
    #left {
        width: 50%;
    }
    #right {
        width: 50%;
    }
    @media screen and (max-width: 1440px) {
        #card {
            flex-direction: column;
            width: 90%;
            height: 700px;
            overflow: visible;
            margin: auto;
        }
        #left {
            width: 100%;
        }
        #right {
            width: 100%;
        }
        #card-wrapper > img {
            display: none;
        }
    }
</style>
