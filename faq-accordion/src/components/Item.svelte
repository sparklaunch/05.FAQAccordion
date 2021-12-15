<script lang="ts">
    export let faq;
</script>

<div class="item">
    <div class="title">{faq.title}</div>
    {#if faq.content}
        <div class="content">{faq.content}</div>
    {/if}
</div>
