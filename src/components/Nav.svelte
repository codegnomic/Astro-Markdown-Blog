<script lang="ts">
    import NavItem from "./NavItem.svelte"
</script>

<nav class="w-full flex bg-slate-300 dark:bg-slate-900 p-1">
    <ul class="flex-grow flex justify-center">
        <NavItem slug="/" title="Home" />
        <NavItem slug="/blog/1" title="Blog" />
        <NavItem slug="/projects" title="Projects" />
        <NavItem slug="/contact" title="Contact" />
    </ul>
</nav>
