<script>
  import Step from "./Step.svelte";

  let steps = [
    {name: 'Chatpdf', icon: 'fa-solid fa-cart-shopping'},
    {name: 'Ultimate Todos', icon: 'fa-solid fa-list-check'},
    {name: 'Poke', icon: 'fa-solid fa-diagram-project'},
  ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi I'm <span class="poppins text-violet-400">Juan</span> Martin <br/> Front-End
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
            My <span class="text-violet-400">favorite tech </span> Includes Javascript (NEXT.JS
            or SvelteKit), TailwindCSS, Node.js + Express.js & PostgreSQL or Firebase/Firestore!
        </p>
        <a class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins
        relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" href="#" target="_blank">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20
        group-hover:translate-x-full xz-0 duration-200"/>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
        </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <!-- <img src={"images/profile.png"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]"/> -->
        </div>
    </section>



    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavour
            </h6>
            <h3 class="font-semibold text-3xl sm:text4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> any work?
            </h3>
        </div>
        <a href="https://www.youtube.com/watch?v=-2UjwQzxvBQ&t=2351s" 
        target="_blank"
        class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
           <i class="fa-regular fa-circle-play "></i>
           <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum pariatur culpa provident!
                   <strong class="text-violet-400">Next.js Commerce.js Stripe & Node.js +Express.js</strong> Est veritatis exercitationem error placeat a laborum aut quaerat optio, iure tenetur accusantium!
                    Expedita doloremque assumenda officia accusamus!
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum pariatur culpa provident!
                    <strong class="text-violet-400">Next.js Commerce.js Stripe & Node.js +Express.js</strong> Est veritatis exercitationem error placeat a laborum aut quaerat optio, iure tenetur accusantium!
                     Expedita doloremque assumenda officia accusamus!
                 </p>
            </Step>
            <Step step={steps[2]}>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum pariatur culpa provident!
                    <strong class="text-violet-400">Next.js Commerce.js Stripe & Node.js +Express.js</strong> Est veritatis exercitationem error placeat a laborum aut quaerat optio, iure tenetur accusantium!
                     Expedita doloremque assumenda officia accusamus!
                 </p>
            </Step>
        </div>
    </section>
    <section id="about">

    </section>
</main>