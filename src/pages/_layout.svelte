<script>
    import Nav from "../components/nav.svelte";
    import Footer from "../components/footer.svelte";
</script>

<!-- routify:options preload="proximity" -->
<Nav/>
<div class="grid place-items-center">
    <main class="w-2/3">
        <slot />
    </main>
</div>
<Footer/>
