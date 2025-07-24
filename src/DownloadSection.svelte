<script>
    import ActionButton from "./lib/ActionButton.svelte";
    import UnderlineTitle from "./lib/UnderlineTitle.svelte";
    import downloaIllustration from './assets/download_app_illustration.png';
</script>

<section class=" mb-28">
    <div class="container flex flex-col-reverse md:flex-row md:items-center md:justify-between gap-16">
        <article class=" md:max-w-[425px] md:p-11">
            <UnderlineTitle text={"Download our mobile apps"} center={false}  />
            <p class="text-md text-gray-500 font-normal mt-6 mb-11">
                Our dedicated patient engagement app and 
                web portal allow you to access information instantaneously (no tedeous form, long calls, 
                or administrative hassle) and securely
            </p>
            <ActionButton text={"Download"} hasIcon={true} />
        </article>

        <figure>
            <img src={downloaIllustration} alt="App download illustration">
        </figure>
    </div>
</section>