<script>
    import ActionButton from "./ActionButton.svelte";
    import heroIllutration from '../assets/header_illustration.png';
    import heroMobileImage from '../assets/heroImageMobile.png';
</script>

<section class=" mb-28">
    <div class="container grid md:grid-cols-2 items-center justify-between ">
        <article class=" mb-16 md:mb-0 md:w-[70%]">
            <h1 class=" text-5xl font-md text-black mb-6">Virtual healthcare for you</h1>
            <p class=" text-gray-500 text-md font-normal mb-11">
                Trafalgar provides progressive, and affordable 
                healthcare, accessible on mobile and online 
                for everyone
            </p>
            <ActionButton text={"Consult today"} fill={true} />
        </article>
        
        <picture>
            <source media="(min-width: 48rem)" srcset={heroIllutration}>
            <img src={heroMobileImage} alt="Hero illustration"> 
        </picture>
    </div>
</section>