<script>
    import Menu from '$lib/Menu.svelte';
    import Footer from '$lib/Footer.svelte';
</script>

<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>



<Menu />
<slot />
<Footer />