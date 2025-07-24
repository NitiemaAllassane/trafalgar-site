<script>
    import leadingImage from '../assets/leading_illustration.png';
  import ActionButton from './ActionButton.svelte';
  import UnderlineTitle from './UnderlineTitle.svelte';
</script>

<section class=" mb-28">
    <div class="container grid grid-cols-1 md:grid-cols-2 justify-center items-center">
        <figure>
            <img src={leadingImage} alt="leading illustration">
        </figure>
        <article class=" mt-10 md:mt-0 md:p-20">
            <UnderlineTitle center={false} text={"Leading healthcare providers"} />
            <p class=" text-md text-gray-500 font-normal mt-6 mb-11">
                Trafalgar provides progressive, and affordable healthcare, accessible on mobile and online for everyone. To us, it’s not just work. We take pride 
                in the solutions we deliver
            </p>
            <ActionButton text={"Learn more"} fill={false} />
        </article>
    </div>
</section>