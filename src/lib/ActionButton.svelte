<script>
    let { text, fill = false, hasIcon = false } = $props();
    import { ArrowDown } from 'lucide-svelte';
</script>

<a href="/" 
    class="inline border-2 border-primary text-primary py-3 px-6
    rounded-[40px] 
    transition duration-200 ease-out
    {fill ? "bg-primary text-white hover:text-primary hover:bg-transparent": "hover:bg-primary hover:text-white "}
    {hasIcon ? " inline-flex items-center justify-center gap-3" : ""}
    "
>
    {text}
    {#if hasIcon}
        <ArrowDown class=" text-md" />
    {/if}
</a>