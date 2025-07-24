<script>
    import Logo from './Logo.svelte';
    import MenuButton from './MenuButton.svelte';
</script>

<header class=" py-10 mb-6">
    <div class="container">
        <div class="flex justify-between items-center">
            <Logo />
            <nav class="hidden md:block">
                <ul class=" flex items-center gap-10">
                    <li><a href="/" class=" text-black">Home</a></li>
                    <li><a href="/" class="text-gray-500 hover:text-black transition duration-300">Find a doctor</a></li>
                    <li><a href="/" class="text-gray-500 hover:text-black transition duration-300">Apps</a></li>
                    <li><a href="/" class="text-gray-500 hover:text-black transition duration-300">Testimonials</a></li>
                    <li><a href="/" class="text-gray-500 hover:text-black transition duration-300">About us</a></li>
                </ul>
            </nav>
            <MenuButton />
        </div>
    </div>
</header>