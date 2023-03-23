<script>
    
    import '../app.css'
    import Header from '$lib/Header.svelte'
    import Footer from '$lib/Footer.svelte'

    let scrollY

</script>

<svelte:window bind:scrollY />

<Header {scrollY} />

<main>
    <slot />
</main>

<Footer />