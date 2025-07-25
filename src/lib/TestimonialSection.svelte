<script lang="ts">
    import Icon from "@iconify/svelte";
    import UnderlineTitle from "./UnderlineTitle.svelte";
    import { fly } from "svelte/transition";

    import edwardImage from '../assets/edward.png';
    import ameliaImage from '../assets/woman.jpg';
    import liamImage from '../assets/man.jpg';
    import sophiaImage from '../assets/woman2.jpg';
    

    /**
     * TODO: Mettre l'image de fond : import bgDecorImage from '../assets/bg-deco2.svg'
     * 
    */



    let testimonials = [
        {
            auteur: "Edward Newgate",
            profession: "Founder Circle",
            message: `“
                Our dedicated patient engagement app and web portal allow you to access 
                information instantaneously (no tedious form, long calls, 
                or administrative hassle) and securely”`,
            avatar: edwardImage,
        },
        {
            auteur: "Amelia Clarkson",
            profession: "Cardiologist",
            message: `“
                This platform has revolutionized how I connect with my patients. 
                The ease of access and security are unmatched in today's digital health space.”`,
            avatar: ameliaImage,
        },
        {
            auteur: "Liam Carter",
            profession: "HealthTech Consultant",
            message: `“
                The user experience is seamless and intuitive. I highly recommend it 
                for anyone serious about modernizing patient communication.”`,
            avatar: liamImage,
        },
        {
            auteur: "Sophia Mendes",
            profession: "Nutritionist",
            message: `“
                I love how the platform simplifies everything—from booking appointments 
                to accessing test results. My clients appreciate it too!”`,
            avatar: sophiaImage,
        }
    ];


    let currentTestimonial: number = $state(0);
    let maxTestimonial: number = testimonials.length;

    function showNexTestimonial(): void {
        currentTestimonial = (currentTestimonial + 1) % maxTestimonial;
    }

    function showPrevTestimonial(): void {
        currentTestimonial = (currentTestimonial - 1 + maxTestimonial) % maxTestimonial;
    }



</script>


<section class="mb-28 md:mb-56">
    <div class="container">
        <div class="bg-gradient-to-b from-gradient-start to-gradient-end p-6 pt-16 md:p-16 rounded-3xl mb-10">
            <UnderlineTitle text={"What our customer are saying"} textColor={"white"} isLineBlack={false} center={true} />
            {#each testimonials as testimonial, index }
                {#if index === currentTestimonial}
                    <article class="mt-6 md:mt-20 grid grid-cols-1 md:grid-cols-2 items-center">
                        <div class="flex flex-col md:flex-row items-center gap-6 mb-6 md:mb-0">
                            <figure 
                                class="w-28 h-28 rounded-full bg-white overflow-hidden 
                                flex items-center justify-center"

                                in:fly={{x: 80}}
                            >
                                <img class=" w-[90%] h-[90%] rounded-full object-cover " src={testimonial.avatar} alt="Edward avatar">
                            </figure>
                            <div 
                                class="text-white text-center md:text-start"
                                in:fly={{x: 90, delay: 100}}
                            >
                                <h4 class="font-bold text-[22px] ">{testimonial.auteur}</h4>
                                <p class="font-normal text-md">{testimonial.profession}</p>
                            </div>
                        </div>

                        <div in:fly={{x: 80, delay: 200}}>
                            <p class="text-white text-[19px] text-center md:text-start font-normal ">
                                {testimonial.message}
                            </p>
                        </div>
                    </article>
                {/if}
            {/each}
        </div>
        <div>
            <form 
                class=" flex items-center justify-center gap-10 md:gap-20"
                onsubmit={(event) => {
                    event.preventDefault();
                }}
            >
                <button type="button" 
                    class="text-2xl text-primary cursor-pointer font-normal p-3 
                    rounded-full border-2 border-primary hover:bg-primary 
                    hover:text-white transition-colors duration-200 ease-out" 

                    onclick={showPrevTestimonial}
                >
                    <Icon icon="mdi:arrow-left" />
                </button>
                <div class="flex gap-3">
                     {#each testimonials as _, i}
                        <input 
                            type="radio" 
                            name="testimonial" 
                            checked={i === currentTestimonial}
                            onchange={() => currentTestimonial = i}
                            class="text-primary accent-primary cursor-pointer"
                        >
                    {/each}
                </div>
                <button type="button" 
                    class="text-2xl text-primary cursor-pointer font-normal p-3 rounded-full border-2 
                    border-primary hover:bg-primary hover:text-white 
                    transition-colors duration-200 ease-out"

                    onclick={showNexTestimonial}
                >
                    <Icon icon="mdi:arrow-right" />
                </button>
            </form>
        </div>
    </div>
</section>