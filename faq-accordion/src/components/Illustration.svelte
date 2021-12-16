<script lang="ts">
    $: innerWidth = 0;
    $: isMobile = innerWidth <= 1440;
</script>

<svelte:window bind:innerWidth />
<div id="illustration">
    <img
        src="/assets/illustration-woman-online-{isMobile
            ? 'mobile'
            : 'desktop'}.svg"
        alt="Illustration"
    />
    <img
        src="/assets/bg-pattern-{isMobile ? 'mobile' : 'desktop'}.svg"
        alt="Background Pattern"
    />
</div>

<style>
    #illustration {
        position: relative;
    }
    #illustration > img:first-child {
        position: absolute;
        width: 100%;
        height: auto;
        top: 25vh;
        left: 10vh;
        transform: translate(-50%, -50%);
    }
    #illustration > img:last-child {
        position: absolute;
        width: 100%;
        top: 30vh;
        left: 10vh;
        transform: translate(-50%, -50%);
    }
    @media screen and (max-width: 1440px) {
        #illustration {
            width: 300px;
            height: auto;
            top: -28vh;
            left: 32.5%;
        }
        #illustration > img:last-child {
            top: 33vh;
        }
    }
    @media screen and (max-width: 650px) {
        #illustration {
            left: 50%;
            transform: translateX(-34%);
        }
    }
</style>
