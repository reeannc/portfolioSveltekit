<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Face and Emotion Detection App', icon: 'fa-thin fa-face-smile'},
        {name: 'Social Media Website Blocker', icon: 'fa-solid fa-computer'},
        {name: 'To be created', icon: 'fa-solid fa-computer'},
    ]

    let benefits = [
        {name: 'a self taught developer', description: 'I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.'},
        {name: '', description: ''},
        {name: '', description: ''},
    ]
    

</script>

<main class="flex flex-col flex-1">
    <section id="introPage" class="px-5 grid grid-cols-1 lg:grid-cols-2 gap-10 py-10 sm:py-6">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Reeann</span> Albert<br/>Web
                        <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-violet-400">favorite tech </span>
                includes JavaScript (SvelteKit) and TailwindCSS, currently learning React
            </p>
            <button
            class="blueShadow border-b-4 border-violet-700 rounded mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group bg-white text-slate-950">
            <div
                class="absolute top-0 right-full w-full h-full bg-yellow-400 opacity-20 group-hover:translate-x-full z-0 duration-300"
            />
            <h4 class="relative z-9">Get in touch &rarr;</h4>
        </button>
        </div>
        <div class="relative shadow-xl grid place-items-center">
            <img
            src={`images/codergirl.png`} 
            alt="Profile image" 
            class="object-cover z-[2] max-h-[70vh]"
            />
        </div>
    </section>

    <section class="py-20 lg:py-40 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center py-100">
        <h6 class="text-large sm:text-xl md:text-2xl">
            A few of my creative endeavors
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Curious to <span class="poppins text-violet-400">see</span>
            my work?
        </h3>
        </div>
        <a href="https://github.com/reeannc"
        target="_blank" class="mx-auto px-4 py-2 rounded-md border
        border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0
        -mt-10 hover:border-violet-700 duration-200">
            <i class="fa-regular fa-circle-play"></i>
            <p>Click the link</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Smoljames Store is a a merchanising store created with <strong
                        class="text-violet-400"
                        >Next.js, Commerce.js, Stripe & Node.js + Express.js!</strong
                    > Commerce.js is a product CMS and Stripe is used for all transaction
                    handling.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Ultimate Todos is a Full Stack <strong
                        class="text-violet-400">Next.js</strong
                    >,
                    <strong class="text-violet-400">Node.js + Express.js</strong
                    >
                    & <strong class="text-violet-400">Firebase</strong> CRUD application
                    that allows a user to login, manage a tidy and efficacious todo
                    list, and persist this information across devices.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Ultimate Todos is a Full Stack <strong
                        class="text-violet-400">Next.js</strong
                    >,
                    <strong class="text-violet-400">Node.js + Express.js</strong
                    >
                    & <strong class="text-violet-400">Firebase</strong> CRUD application
                    that allows a user to login, manage a tidy and efficacious todo
                    list, and persist this information across devices.
                </p>
            </Step>
        </div>
    </section>
    
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col
    gap-16 sm:gap-10 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute
        before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
        after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 
        after:bg-violet-700 py-4">
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-violet-400">
            about </span>me
        </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am ...</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>{benefit.description}</p>
                </div>
            </div>
            {/each}
        </div>
    </section>
</main>