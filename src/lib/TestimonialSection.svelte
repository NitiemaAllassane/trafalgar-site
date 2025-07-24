<script>
    import UnderlineTitle from "./UnderlineTitle.svelte";
    import edwardImage from '../assets/edward.png';

    /**
     * !import bgDecorImage from '../assets/bg-deco2.svg'
     * TODO:  fonctionner le caroussel de testiminial.
    */

    
    
    import Icon from "@iconify/svelte";

    let currentTestimonial = $state(1);

    let testimonials = [
        {
            auteur: "Edward Newgate",
            profession: "Founder Circle",
            message: `“
                Our dedicated patient engagement app and web portal allow you to access 
                information instantaneously (no tedious form, long calls, 
                or administrative hassle) and securely”`,
            avatar: edwardImage,
        }
    ];

</script>


<section class="mb-28 md:mb-56">
    <div class="container">
        <div class="bg-gradient-to-b from-gradient-start to-gradient-end p-6 pt-16 md:p-16 rounded-3xl mb-10">
            <UnderlineTitle text={"What our customer are saying"} textColor={"white"} isLineBlack={false} center={true} />
            {#each testimonials as testimonial }
                <article class="mt-6 md:mt-20 grid grid-cols-1 md:grid-cols-2 items-center">
                    <div class="flex flex-col md:flex-row items-center gap-6 mb-6 md:mb-0">
                        <figure class="w-28 h-28 rounded-full bg-white overflow-hidden flex items-center justify-center">
                            <img class=" w-[90%] h-[90%] rounded-full " src={testimonial.avatar} alt="Edward avatar">
                        </figure>
                        <div class="text-white text-center md:text-start">
                            <h4 class="font-bold text-[22px] ">{testimonial.auteur}</h4>
                            <p class="font-normal text-md">{testimonial.profession}</p>
                        </div>
                    </div>

                    <div>
                        <p class="text-white text-[19px] text-center md:text-start font-normal ">
                            {testimonial.message}
                        </p>
                    </div>
                </article>
            {/each}
        </div>
        <div>
            <form class=" flex items-center justify-center gap-10 md:gap-20">
                <button type="button" class="text-2xl text-primary cursor-pointer font-normal p-3 rounded-full border-2 border-primary hover:bg-primary hover:text-white transition-colors duration-200 ease-out" >
                    <Icon icon="mdi:arrow-left" />
                </button>
                <div class="flex gap-3">
                    <input type="radio" name="testimonial" id="1"class="text-primary accent-primary cursor-pointer" checked>
                    <input type="radio" name="testimonial" id="2"class="text-primary accent-primary cursor-pointer">
                    <input type="radio" name="testimonial" id="3"class="text-primary accent-primary cursor-pointer">
                    <input type="radio" name="testimonial" id="4"class="text-primary accent-primary cursor-pointer">
                </div>
                <button type="button" class="text-2xl text-primary cursor-pointer font-normal p-3 rounded-full border-2 border-primary hover:bg-primary hover:text-white transition-colors duration-200 ease-out">
                    <Icon icon="mdi:arrow-right" />
                </button>
            </form>
        </div>
    </div>
</section>