<script>
    import UnderlineTitle from './UnderlineTitle.svelte';

    import searchIcon from '../assets/search-icon.svg';
    import pharmacyIcon from '../assets/pharmacy-icon.svg';
    import consultationIcon from '../assets/consultation-icon.svg';
    import infoIcon from '../assets/info.svg';
    import emergencyIcon from '../assets/emergency-icon.svg';
    import trackingIcon from '../assets/tracking-icon.svg';
  import ActionButton from './ActionButton.svelte';
    


    const services = [
        {
            title: "Search doctor",
            paragraph: "Choose your doctor from thousands of specialist, general, and trusted hospitals",
            image: searchIcon
        },

        {
            title: "Online pharmacy",
            paragraph: "Buy  your medicines with our mobile application with a simple delivery system",
            image: pharmacyIcon
        },

        {
            title: "Consultation",
            paragraph: "Free consultation with our trusted doctors and get the best recomendations",
            image: consultationIcon
        },

        {
            title: "Details info",
            paragraph: "Free consultation with our trusted doctors and get the best recomendations",
            image: infoIcon
        },

        {
            title: "Emergency care",
            paragraph: "You can get 24/7 urgent care for yourself or your children and your lovely family",
            image: emergencyIcon
        },

        {
            title: "Tracking",
            paragraph: "Track and save your medical history and health data ",
            image: trackingIcon
        },
    ];
</script>

<section>
    <div class="container">
        <header class=" mb-20">
            <div class=" max-w-3xl mx-auto">
                <UnderlineTitle center={true} />
                <p class="text-gray-500 text-center text-md font-normal mt-6">
                    We provide to you the best choiches for you. 
                    Adjust it to your health needs and make sure your undergo treatment with our 
                    highly qualified doctors you can consult with us which type of service is suitable for your health
                </p>
            </div>
        </header>

        <section class=" grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 lg:gap-6 mb-20">
            {#each services as card }
                <article class=" w-auto md:w-[350px] p-6 md:p-11 shadow-[5px_16px_64px_rgba(0,0,0,0.1)] rounded-3xl ">
                    <figure class=" mb-6">
                        <img src={card.image} alt="search icon illustration">
                    </figure>
                    <h3 class=" text-2xl font-bold text-black mb-4">
                        {card.title}
                    </h3>
                    <p class=" text-gray-500 text-[16px] font-normal">
                        {card.paragraph}
                    </p>
            </article>
            {/each}
        </section>
    </div>
    <div class="block text-center">
        <ActionButton fill={false} text={"Learn more"} />
    </div>
</section>