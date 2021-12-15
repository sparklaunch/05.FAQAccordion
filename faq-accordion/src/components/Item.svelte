<script lang="ts">
    export let faq;
    let isOpen: boolean = true;
    const clickHandler: () => void = () => {
        if (faq.isActive) {
            isOpen = !isOpen;
        }
    };
</script>

<div class="item">
    <div class="title" class:active={faq.isActive} on:click={clickHandler}>
        <p>{faq.title}</p>
        <img
            src="/assets/icon-arrow-down.svg"
            alt="Down Arrow"
            class:opposite={faq.isActive && isOpen}
        />
    </div>
    {#if faq.content && faq.isActive}
        <div class="content" class:open={!isOpen}>
            {faq.content}
        </div>
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
        cursor: pointer;
    }
    .item > .title > p {
        color: rgb(77, 76, 82);
        padding: 20px 0;
        transition: color 0.3s;
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
        transition: ease all 0.3s;
        position: relative;
        height: auto;
        opacity: 1;
        z-index: 0;
    }
    .active {
        font-weight: 700;
    }
    .opposite {
        transform: rotate(180deg);
    }
    .open {
        height: 0 !important;
        margin: 0 !important;
        opacity: 0 !important;
        z-index: -1 !important;
    }
</style>
