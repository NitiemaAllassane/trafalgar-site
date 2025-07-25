<script>
    import { Menu } from "lucide-svelte";
    let { doAction } = $props();
</script>

<button class="md:hidden" onclick={doAction} >
    <Menu />
</button>