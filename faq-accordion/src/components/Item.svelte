<script lang="ts">
    export let faq;
</script>

<div class="item">
    <div class="title" class:active={faq.isActive}>
        <p>{faq.title}</p>
        <img
            src="/assets/icon-arrow-down.svg"
            alt="Down Arrow"
            class:opposite={faq.isActive}
        />
    </div>
    {#if faq.content && faq.isActive}
        <div class="content">{faq.content}</div>
    {/if}
</div>

<style>
    .item {
        border-bottom: 1px solid rgb(229, 229, 299);
    }
    .item > .title {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .item > .title > p {
        color: rgb(77, 76, 82);
        padding: 20px 0;
        transition: color 0.3s;
        cursor: pointer;
    }
    .item > .title > p:hover {
        color: rgb(198, 134, 117);
    }
    .item > .title > img {
        width: 15px;
        height: 10px;
        transition: transform 0.5s;
    }
    .item > .content {
        color: rgb(119, 118, 124);
        margin-bottom: 20px;
    }
    .active {
        font-weight: 700;
    }
    .opposite {
        transform: rotate(180deg);
    }
</style>
