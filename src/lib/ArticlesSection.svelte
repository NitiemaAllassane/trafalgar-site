<script>
    import Icon from "@iconify/svelte";
    import UnderlineTitle from "./UnderlineTitle.svelte";

    import articleImage1 from '../assets/article1.png';
    import articleImage2 from '../assets/article2.png';
    import articleImage3 from '../assets/article3.png';
  import ActionButton from "./ActionButton.svelte";

    let articles = [
        {
            image: articleImage1,
            title: "Disease detection, check up in the laboratory",
            introduction: "In this case, the role of the health laboratory is very important to doa disease detection..."
        },

        {
            image: articleImage2,
            title: "Herbal medicines that are safe for consumption",
            introduction: "Herbal medicine is very widely used at this time because of its very good for your health..."
        },

        {
            image: articleImage3,
            title: "Natural care for healthy facial skin",
            introduction: "A healthy lifestyle should start from now and also for your skin health. There are some..."
        },
    ]

</script>


<section class=" mb-56">
    <div class="container">
        <UnderlineTitle  text={"Check out our latest article"} center={true} />
        <div class=" mt-16 mb-16 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 md:gap-6 ">
            {#each articles as article }
                <article class=" w-auto md:w-[350px] rounded-[20px] bg-white shadow-[0_4px_64px_rgba(0,0,0,0.1)] ">
                    <figure class=" overflow-hidden max-w-full rounded-t-[20px] ">
                        <img src={ article.image } alt="Person's vaccination" class="w-full h-full object-cover">
                    </figure>
                    <div class=" p-8">
                        <h3 class=" text-2xl font-md text-black mb-3">{ article.title }</h3>
                        <p class=" text-gray-500 font-normal mb-6">
                            { article.introduction }
                        </p>
                        <a href="/" class=" inline-flex items-center text-primary font-semibold gap-3 hover:text-gradient-start transition duration-150 ease">
                            <span>Read more</span>
                            <Icon icon="mdi:arrow-right" />
                        </a>
                    </div>
                </article>
            {/each}
        </div>
        <div class=" block text-center">
            <ActionButton text={"View all"}  />
        </div>
    </div>
</section>