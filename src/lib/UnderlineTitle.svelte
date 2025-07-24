<script>
    let { center = false, text, lineColor = "black", textColor="black" } = $props();
</script>

<h2 class="
    relative {center ? "text-center after:left-1/2 after:-translate-x-1/2" : "after:left-0"} 
    text-4xl font-medium pb-10 text-{textColor}
    after:content-[''] after:absolute after:bottom-4 after:w-[64px] 
    after:h-[3px] after:bg-{lineColor}
">
    {text}
</h2>