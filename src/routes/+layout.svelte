<script>
    import Header from '$lib/Header.svelte';
    import Footer from '$lib/Footer.svelte';
</script>

<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<div class="nav">
    <input type="checkbox">
      <span></span>
      <span></span>
      <div class="menu">
        <li><a href="#">home</a></li>
        <li><a href="#">about</a></li>
        <li><a href="#">cursos</a></li>
        <li><a href="#">blog</a></li>
        <li><a href="#">contactos</a></li>
      </div>
</div>

<Header/>

<slot />

<Footer/>