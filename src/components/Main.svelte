<script>
  import Step from "./Step.svelte";

  let steps = [
    {name: 'Chatpdf', icon: 'fa-solid fa-cart-shopping'},
    {name: 'Shopping Cart', icon: 'fa-solid fa-list-check'},
    {name: 'Movie Search', icon: 'fa-solid fa-diagram-project'},
  ]

  let benefits = [
    {name: 'a self taught developer', description: 'passionate about building functional and visually appealing websites. I’ve dived deep into full-stack development, exploring everything from frontend frameworks like React to backend databases and APIs. I’ve also picked up some skills in cybersecurity and Linux along the way, which come in handy for ensuring smooth and secure projects. I love learning new technologies, solving problems, and constantly improving my craft.'},
    {name: 'a web3 and crypto finatic', description: 'who s all about exploring the future of decentralized tech. From diving into blockchain development to keeping up with the latest trends in crypto, I’m always looking for ways to integrate these innovations into real-world applications. I love the idea of building for a decentralized future and believe Web3 is the next big step in tech evolution.'},
    {name: 'an excelent comunicator', description: 'who loves connecting with people and making complex ideas easy to understand. Whether it s collaborating with a team, explaining technical concepts, or just making sure everyone s on the same page, I enjoy creating clear and effective communication. I believe good communication is key to solving problems and building strong relationships, both in work and life.'},
  ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi I'm <span class="poppins text-violet-400">Juan</span> Martin <br/> Front-End
                <span class="poppins text-violet-400">Software Developer </span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
            My <span class="text-violet-400">favorite tech </span> Includes  <span class="text-violet-400">Javascript (NEXT.JS), TailwindCSS, Node.js + Express.js & PostgreSQL or Firebase!</span>  Apart from coding, some other activities that I love to do!
            playing video games,
            writing poetry and novels,
            train in the gym.
        </p>
        <!-- <a class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins
        relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" 
        href="#about" 
        target="_blank"
        >
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20
        group-hover:translate-x-full xz-0 duration-200"/>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
        </a> -->
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.png"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]"/>
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
        <a href="https://github.com/SaraviaMartin?tab=repositories" 
        target="_blank"
        class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
           <i class="fa-regular fa-circle-play "></i>
           <p>Watch my repos</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Development of a tool that allows interaction through chat with PDF files, making it easier to extract and query information dynamically.
                   <strong class="text-violet-400">Next.js, TypeScript, Clerk, Neon DB, Tailwind CSS, OpenAI API, y Vercel.</strong>  
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>Shopping cart simulation created with React, which allows showing a product list, filtering by price and category, and managing the cart. Users can add, remove, or change the quantity of products, with real-time updates synced with the list.
                    <strong class="text-violet-400">React, HTML, CSS.</strong> 
                 </p>
            </Step>
            <Step step={steps[2]}>
                <p>Web application developed to search movies and get detailed information using the OMDb API.
                    <strong class="text-violet-400">React, HTML, CSS, JavaScript.</strong> 
                 </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0
        before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0
        after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            A bit <span class="poppins text-violet-400"> about </span>me.
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
    <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            The <span class="text-violet-400">Complete</span> Package
        </h5>
        <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th
                            class="bg-violet-700 text-white whitespace-nowrap p-4 px-8"
                            >Me</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Critical Thought</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Interpersonal Skills</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Progamming Ability</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
    </section>
</main>