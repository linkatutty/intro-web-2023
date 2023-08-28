<script>
    import Header from '$lib/Header.svelte';
    import Menu from '$lib/Menu.svelte';
    import Nav from '$lib/nav.svelte';
    import Footer from '$lib/Footer.svelte';
</script>

<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>



<Menu />
<!-- <Nav /> -->
<slot />
<Footer />