<script lang="ts">
    import Icon from "@iconify/svelte"
    import sunDuotone from "@iconify/icons-ph/sun-duotone"
    import moonStarsDuotone from "@iconify/icons-ph/moon-stars-duotone"
    import NavItem from "./NavItem.svelte"
    import { darkmode } from "src/stores"

    const handleDarkmodeToggle = () => {
        darkmode.set(!$darkmode)
    }
</script>

<nav class="w-full flex bg-slate-300 dark:bg-slate-900 dark:text-slate-100 p-1">
    <ul class="flex-grow flex justify-center">
        <NavItem slug="/" title="Home" />
        <NavItem slug="/blog/1" title="Blog" />
        <NavItem slug="/projects" title="Projects" />
        <NavItem slug="/contact" title="Contact" />
    </ul>
    <button on:click={handleDarkmodeToggle}>
        {#if $darkmode}
            <Icon icon={sunDuotone} />
        {:else}
            <Icon icon={moonStarsDuotone} />
        {/if}
    </button>
</nav>
