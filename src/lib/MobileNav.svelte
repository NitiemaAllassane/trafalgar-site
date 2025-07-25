<script>
    import Logo from "./Logo.svelte";
    import Icon from "@iconify/svelte";

    import { mobileNav } from "../globalState.svelte";
    import { fly } from "svelte/transition";

    function closeMobileNav() {
        if( mobileNav.isOpen === false ) return;
        mobileNav.isOpen = false;
    }
</script>

<!-- * OVERLAY -->
<div class="fixed top-0 left-0 bg-black opacity-60 w-full h-full md:hidden" ></div>

<nav 
    class=" fixed top-0 left-0 z-40 bg-gradient-to-l from-gradient-start 
    to-gradient-end w-[70%] h-[100vh] pt-9 shadow-[6px_0_64px_rgba(0,0,0,0.1)]
    md:hidden"

    transition:fly={{x: -250, duration: 450}}
>
    <div class="container">
        <Logo />
        <ul class=" mt-10 flex flex-col gap-3">
            <li><a href="/" class=" text-white">Home</a></li>
            <li><a href="/" class="text-white">Find a doctor</a></li>
            <li><a href="/" class="text-white">Apps</a></li>
            <li><a href="/" class="text-white">Testimonials</a></li>
            <li><a href="/" class="text-white">About us</a></li>
        </ul>
    </div>
</nav>

<button 
    class=" fixed top-[8%] right-[5%] text-3xl font-bold text-white md:hidden "
    onclick={closeMobileNav}
>
    <Icon icon="mdi:close" />
</button>
