<script>
    export let y;

    export let tabs = [
        { name: "Projects", link: "#projects" },
        { name: "About me", link: "#about" },
        { name: "Blog", link: "https://www.youtube.com/watch?v=K4TfMeUxmK4" },
        //{ name: "Contact", link: "#contact" },
        // { name: '', link: '' },
    ];

    function redirectToLinkedIn() {
        //window.location.href = "https://www.linkedin.com/in/biplob-das/";
        const contactSection = document.getElementById('contact');
        if (contactSection) {
            contactSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    function redirectToMainPage() {
        window.location.href = "/"; // Replace "/" with the actual path of your main page
    }
    
</script>
<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-violet-950"
            : " py-6 bg-transparent border-transparent")}
>
<a href="/" class="duration-200 hover:text-violet-400">
    <h1 class="font-medium">
        <b class="font-bold poppins">Biplob's</b><span class="poppins text-violet-400">info</span>page
    </h1>
</a>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-400"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <button
            on:click={redirectToLinkedIn}
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Contact</h4>
        </button>
    </div>
</header>
