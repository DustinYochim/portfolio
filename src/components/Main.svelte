<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Truck Management System",
            icon: "fa-solid fa-truck",
            description:
                "Developed a Java-based Object-Oriented Truck Management System, leveraging OOP principles of encapsulation, inheritance, and polymorphism.",
        },
        {
            name: "Utlimate Task List Application",
            icon: "fa-solid fa-list-check",
            description:
                "Test for model robustness with customized test profiles and receive exhaustive reporting on the performance and potential vulnerabilities of your model.",
        },
        {
            name: "Tic Tac Toe",
            icon: "fa-solid fa-gamepad",
            description:
                "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "a senior in University",
            description:
                "As a senior in university pursuing a degree in computer science, I have cultivated a comprehensive understanding of foundational principles and advanced concepts, honing my analytical and problem-solving skills to tackle complex challenges within the dynamic realm of computer science.",
        },
        {
            name: "a dedicated life long learner",
            description:
                "Dedicated to a lifelong journey of learning and growth in the ever-evolving field of computer science, I embrace challenges as opportunities to expand my knowledge and skills, staying committed to continuous improvement and staying at the forefront of technological advancements.",
        },
        {
            name: "an excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Dustin</span> Yochim
                <br />CS
                <span class="poppins text-violet-400">Student</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400"> favorite classes</span> so far have been Object-Oriented Programming, Full Stack 
                Web Development, and Data Structures and Algorithms!
            </p>
            <button
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <a href="mailto:Yochim.Dustin@gmail.com"><h4 class="relative z-9">Get in touch &rarr;</h4></a>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile1.jpeg"}
                alt="Dustin Yochim"
                class="object-cover z-[2] max-h-[70vh] profile"
            />
        </div>

    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <!-- <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my endeavors.
            </h6> -->
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                My Recent <span class="poppins text-violet-400">Projects</span>
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Developed a <strong class="text-violet-400">Java-based Object-Oriented</strong> Truck Management System, leveraging OOP principles of encapsulation,
                    inheritance, and polymorphism.</p>
            
            </Step>
            <Step step={steps[1]}>
                <p>
                    Crafted an <strong class="text-violet-400">innovative and dynamic</strong> to-do list application through the meticulous design and development process, employing vanilla JS, HTML, and CSS to showcase proficiency in creating <strong class="text-violet-400">intuitive and responsive</strong> user interfaces.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Developed an interactive Tic Tac Toe application featuring <strong class="text-violet-400">AI</strong> opponents with varying difficulty levels, employing
                    <strong class="text-violet-400">advanced algorithms</strong> like random moves, <strong class="text-violet-400">minimax</strong>, and <strong class="text-violet-400">Monte Carlo search tree</strong>. Implemented using vanilla HTML, CSS, and JS, showcasing expertise in front-end technologies and game development strategies.
                </p>
                
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <!-- <div class="flex flex-col gap-2 mx-auto">
                    <div class="flex items-end gap-4">
                        <p
                            class="poppins text-6xl sm:text-7xl md:text-8xl text-slate-500 font-medium"
                        >
                            {benefit.metric}
                        </p>
                        <p
                            class="text-xl sm:text-2xl md:text-3xl capitalize pb-2"
                        >
                            {benefit.name}
                        </p>
                    </div>
                    <p class="text-center italic">- {benefit.description}</p>
                </div> -->
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
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
        
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        
    </section>
</main>
