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
