<script lang="ts">
    import { darkmode } from "src/stores"
</script>

<div class={`${$darkmode ? "dark" : ""} w-screen h-screen flex flex-col`}>
    <slot />
</div>
