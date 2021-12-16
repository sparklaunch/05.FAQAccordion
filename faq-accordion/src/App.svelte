<script lang="ts">
    import Card from "./components/Card.svelte";
    interface FAQ {
        title: string;
        content?: string;
        isActive: boolean;
    }
    const faqs: FAQ[] = [
        {
            title: "How many team members can I invite?",
            isActive: false,
        },
        {
            title: "What is the maximum file upload size?",
            content:
                "No more than 2GB. All files in your account must fit your allotted storage space.",
            isActive: true,
        },
        {
            title: "How do I reset my password?",
            isActive: false,
        },
        {
            title: "Can I cancel my subscription?",
            isActive: false,
        },
        {
            title: "Do you provide additional support?",
            isActive: false,
        },
    ];
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
    <Card data={faqs} />
</div>

<style>
    #app {
        width: 100vw;
        height: 100vh;
        background: linear-gradient(rgb(166, 93, 231), rgb(90, 88, 229));
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }
</style>
