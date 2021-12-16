<script lang="ts">
    import Item from "./Item.svelte";
    export let data;
</script>

<div id="faq">
    <h1>FAQ</h1>
    <div id="faqs">
        {#each data as faq}
            <Item {faq} />
        {/each}
    </div>
</div>

<style>
    #faq {
        padding: 50px;
        padding-left: 0;
    }
    #faq > h1 {
        margin-bottom: 30px;
        color: rgb(30, 28, 49);
    }
    @media screen and (max-width: 1440px) {
        #faq {
            padding: 30px;
            margin-top: 100px;
        }
        #faq > h1 {
            text-align: center;
            font-size: 36px;
        }
    }
</style>
