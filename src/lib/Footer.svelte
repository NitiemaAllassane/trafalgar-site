<script>
    import logoLight from '../assets/logo-light.png'
</script>

<footer class="bg-gradient-to-b from-gradient-start to-gradient-end text-white py-16">
    <div class="container">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-20">
            <!-- Section gauche - Logo et description -->
            <div class="space-y-6">
                <img src={logoLight} alt="Trafalgar logo" class="h-12">
                <p class="text-lg font-light leading-relaxed max-w-md">
                    Trafalgar provides progressive, and affordable healthcare, accessible on mobile and online 
                    for everyone
                </p>
                <!-- Copyright -->
                <p class="text-sm opacity-75">
                    &copy;Trafalgar PTY LTD 2020. All rights reserved
                </p>
            </div>

            <!-- Section droite - Liens -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div>
                    <h4 class="text-xl font-bold mb-4">Company</h4>
                    <ul class="space-y-3">
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">About</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Testimonials</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Find a doctor</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Apps</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-xl font-bold mb-4">Region</h4>
                    <ul class="space-y-3">
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Indonesia</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Singapore</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Hongkong</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Canada</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-xl font-bold mb-4">Help</h4>
                    <ul class="space-y-3">
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Help center</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Contact support</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">Instructions</a></li>
                        <li><a href="/" class="text-white hover:text-primary transition-colors duration-200">How it works</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</footer>