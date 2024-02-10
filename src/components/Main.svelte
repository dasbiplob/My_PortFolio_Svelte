<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Smoljames Store",
            icon: "fa-solid fa-cart-shopping",
            description:
                "Smoljames Store is a a merchanising store created with Next.js, Commerce.js & Stripe! Commerce.js is a CMS for managing project and Stripe is used for all transaction handling.",
        },
        {
            name: "Utlimate Todos",
            icon: "fa-solid fa-list-check",
            description:
                "Test for model robustness with customized test profiles and receive exhaustive reporting on the performance and potential vulnerabilities of your model.",
        },
        {
            name: "Pokédex",
            icon: "fa-solid fa-diagram-project",
            description:
                "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "a versatile IT professional with 11+ years of expertise",
            description:
                //"I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.",
                "As a Full Stack Developer leads end-to-end web app development, excelling in Java, JS, React, Svelte, HTML, CSS, and frameworks. Responsibilities span architecture, database integration, mentorship, and staying updated on tech trends. Cloud expertise enhances deployment in secure, scalable environments.",
        },
        {
            name: "a full stack and UiPath developer",
            description:
                //"Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
                "Experienced Full Stack Developer with a passion for coding and diverse skills like Svelte, Java, JS, React. Led a team, established RPA COE, managed 100+ servers and processes, and excelled in client-facing roles. Expert in UiPath, Python, and automation, ensuring innovative solutions and 10% cost reduction. Recognized for resolving critical issues and awarded On The Spot 2022 for addressing log4j vulnerability. Proven track record in solution design, code reviews, and infrastructure management, resulting in a 20% increase in client acceptance. Actively engaged with UiPath product teams, contributing to the product roadmap.",
        },
        {
            name: "an excellent communicator",
            description:
                "Effective communication is a cornerstone of my professional ethos, placing a premium on transparency and constructive dialogue. I prioritize fostering meaningful relationships to enhance both my effectiveness and productivity within any team or work environment.",
        },
    ];

    function redirectToLinkedIn() {
        window.location.href = "https://www.linkedin.com/in/biplob-das/";
    }
    function redirectToFiver() {
        window.location.href = "https://www.fiverr.com/?source=top_nav/";
    }
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
                Hi! I'm <span class="poppins text-violet-400">Biplob</span> Das
                <br />Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400"> favorite tech</span> includes Java + Springboot,JavaScript
                (SvelteKit), React, TailwindCSS, Node.js + Express.js & PostgreSQL
                or Firebase/Firestore!
            </p>
            <div class="flex justify-center items-center">
                    <button on:click={redirectToLinkedIn} class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200" />
                        <h4 class="relative z-9">Get in touch &rarr;</h4>
                    </button>
            
                    <button on:click={redirectToFiver} class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200" />
                        <h4 class="relative z-9">Hire Me &rarr;</h4>
                    </button>
            </div>
            
        </div>

        <div class="flex w-full h-full relative shadow-2xl grid place-items-center">
            <!-- Profile Image -->
            <img
              src="images/profile.png"
              alt="Zetane Engine"
              loading="lazy"
              decoding="async"
              data-nimg="1"
              style="color:transparent"
              class="z-50 relative rounded-full object-cover max-h-[70vh]"
            />
          </div>
        <!-- <div  class="flex p-0.5 relative max-w-[700px] w-full mx-auto">
            <div
                class="absolute inset-0 overflow-hidden rounded-md flex items-center justify-center"
            >
                <div
                    class="bg-gradient-to-r absolute inset-[-20px]  from-violet-800 to-indigo-800 specialSpin"
                />
            </div>

            <img
                src={"images/zetane-engine.jpeg"}
                alt="Zetane Engine"
                class="w-full h-full object-cover z-[2]"
            />
        </div> -->
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a
            href="https://www.youtube.com/watch?v=uYXQwSVTlJU"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
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
                    The Pokédex is a <strong class="text-violet-400"
                        >SvelteKit & TailwindCSS</strong
                    >
                    web application, hosted on
                    <strong class="text-violet-400">Netlify</strong>, that
                    consumes and caches the
                    <strong class="text-violet-400">Pokémon API</strong>
                    to display all Pokémon information. Gotta catch them all!
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
        <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want I know.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                My <span class="poppins text-violet-400">Skills</span> .
            </h3>
        </div>
        <div id="skills" class="px-4 py-16 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 lg:py-20">
            <div class="max-w-xl mb-10 md:mx-auto text-center lg:max-w-2xl md:mb-12">
                <h2 class="max-w-lg mb-6 font-sans text-3xl font-bold leading-none tracking-tight text-gray-900 sm:text-4xl md:mx-auto">
                    <span class="relative inline-block">
                        <svg viewBox="0 0 52 24" fill="currentColor" class="absolute top-0 -right-28 z-0 hidden w-32 -mt-8 -ml-20 text-blue-gray-100 lg:w-32 lg:-ml-28 lg:-mt-10 sm:block">
                            <defs>
                                <pattern id="df31b9f6-a505-42f8-af91-d2b7c3218e5c" x="0" y="0" width=".135" height=".30">
                                    <circle cx="1" cy="1" r=".7"></circle>
                                </pattern>
                            </defs>
                            <rect fill="url(#df31b9f6-a505-42f8-af91-d2b7c3218e5c)" width="52" height="24"></rect>
                        </svg>
                    </span>
                </h2>
            </div>
            <div class="grid gap-8 row-gap-8 lg:grid-cols-3">
                <!-- FrontEnd -->
                <div class="text-center">
                    <!-- FrontEnd content -->
                    <div class="flex items-center justify-center w-16 h-16 mb-4 rounded-full bg-indigo-50 mx-auto sm:w-24 sm:h-24">
                      <i class="fab fa-html5 text-blue-700 text-4xl" aria-hidden="true"></i>
                    </div>
                    <h6 class="mb-2 font-semibold leading-5 border-b-2 pb-4">FrontEnd</h6>
                    <div class="inline-flex mr-2">
                        <object data="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white" class="my-1" aria-label="HTML5 badge"></object>
                    </div>
                    <!-- Add other FrontEnd shields here -->
                    <!-- CSS3 Badge -->
<div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white" class="my-1" aria-label="CSS3 Badge"></object>
  </div>
  
  <!-- JavaScript Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E" class="my-1" aria-label="JavaScript Badge"></object>
  </div>
  
  <!-- TypeScript Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" class="my-1" aria-label="TypeScript Badge"></object>
  </div>
  
  <!-- React Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB" class="my-1" aria-label="React Badge"></object>
  </div>
  
  <!-- Redux Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/redux-%23593d88.svg?style=for-the-badge&logo=redux&logoColor=white" class="my-1" aria-label="Redux Badge"></object>
  </div>
  
  <!-- Svelte Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white" class="my-1" aria-label="Svelte Badge"></object>
  </div>
  
  <!-- Tailwind CSS Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white" class="my-1" aria-label="Tailwind CSS Badge"></object>
  </div>
  
  <!-- Bootstrap Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white" class="my-1" aria-label="Bootstrap Badge"></object>
  </div>
  
  <!-- jQuery Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white" class="my-1" aria-label="jQuery Badge"></object>
  </div>
  
  <!-- Angular Badge -->
  <div class="inline-flex mr-2">
    <object data="https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white" class="my-1" aria-label="Angular Badge"></object>
  </div>
                  </div>
                <!-- BackEnd -->
                <div class="text-center">
                    <!-- ... your existing BackEnd content ... -->
                    <div class="flex items-center justify-center w-16 h-16 mb-4 rounded-full bg-indigo-50 mx-auto sm:w-24 sm:h-24">
                      <i class="fa-solid fa-code text-blue-700 text-4xl" aria-hidden="true"></i>
                    </div>
                    <h6 class="mb-2 font-semibold leading-5 border-b-2 pb-4">BackEnd</h6>
                    <div class="inline-flex mr-2">
                      <img src="https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white" class="my-1" alt="Node.js Badge">
                    </div>
                    <div class="inline-flex mr-2">
                      <img src="https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB" class="my-1" alt="Express Badge">
                    </div>
                    <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/deno%20js-000000?style=for-the-badge&logo=deno&logoColor=white" class="my-1" alt="Deno Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white" class="my-1" alt="Java Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?logo=springboot&logoColor=fff&style=for-the-badge" class="my-1" alt="Spring Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Spring%20Security-6DB33F?logo=springsecurity&logoColor=fff&style=for-the-badge" class="my-1" alt="SpringSecurity Badge">
                      </div>
                    <div class="inline-flex mr-2">
                      <img src="https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=fff&style=for-the-badge" class="my-1" alt="MySQL Badge">
                    </div>
                    <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=fff&style=for-the-badge" class="my-1" alt="Postgressql Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=fff&style=for-the-badge" class="my-1" alt="MongoDB Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff&style=for-the-badge" class="my-1" alt="Python Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Flyway-CC0200?logo=flyway&logoColor=fff&style=for-the-badge" class="my-1" alt="Flyway Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?logo=apachekafka&logoColor=fff&style=for-the-badge" class="my-1" alt="Kafka Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/JSON-000?logo=json&logoColor=fff&style=for-the-badge" class="my-1" alt="Json Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/JSON%20Web%20Tokens-000?logo=jsonwebtokens&logoColor=fff&style=for-the-badge" class="my-1" alt="JWT Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?logo=apachekafka&logoColor=fff&style=for-the-badge" class="my-1" alt="Kafka Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Auth0-EB5424?logo=auth0&logoColor=fff&style=for-the-badge" class="my-1" alt="Auth0 Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Swagger-85EA2D?logo=swagger&logoColor=000&style=for-the-badge" class="my-1" alt="Swagger Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Auth0-EB5424?logo=auth0&logoColor=fff&style=for-the-badge" class="my-1" alt="Auth0 Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/JUnit5-25A162?logo=junit5&logoColor=fff&style=for-the-badge" class="my-1" alt="Junit Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/InfluxDB-22ADF6?logo=influxdb&logoColor=fff&style=for-the-badge" class="my-1" alt="InfluxDb Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Hibernate-59666C?logo=hibernate&logoColor=fff&style=for-the-badge" class="my-1" alt="Hibernate Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Elasticsearch-005571?logo=elasticsearch&logoColor=fff&style=for-the-badge" class="my-1" alt="ELK Badge">
                      </div>
                    <!-- Add similar img tags for the rest of the badges -->
                  </div>
                <!-- Tools -->
                <div class="text-center">
                    <!-- ... your existing Tools content ... -->
                    <div class="flex items-center justify-center w-16 h-16 mb-4 rounded-full bg-indigo-50 mx-auto sm:w-24 sm:h-24">
                        <i class="fa-solid fa-screwdriver-wrench text-blue-700 text-4xl" aria-hidden="true"></i>
                      </div>
                      <h6 class="mb-2 font-semibold leading-5 border-b-2 pb-4">Tools</h6>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=fff&style=for-the-badge" class="my-1" alt="Git Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=fff&style=for-the-badge" class="my-1" alt="GitHub Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/GitLab-FC6D26?logo=gitlab&logoColor=fff&style=for-the-badge" class="my-1" alt="GitLab Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?logo=githubactions&logoColor=fff&style=for-the-badge" class="my-1" alt="GitHubAction Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=fff&style=for-the-badge" class="my-1" alt="Jenkins Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=fff&style=for-the-badge" class="my-1" alt="Docker Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=fff&style=for-the-badge" class="my-1" alt="Kubernetes Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Heroku-430098?logo=heroku&logoColor=fff&style=for-the-badge" class="my-1" alt="Heroku Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Playwright-2EAD33?logo=playwright&logoColor=fff&style=for-the-badge" class="my-1" alt="Playwright Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/GitLab-FC6D26?logo=gitlab&logoColor=fff&style=for-the-badge" class="my-1" alt="GitLab Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Render-46E3B7?logo=render&logoColor=000&style=for-the-badge" class="my-1" alt="Render Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Serverless-FD5750?logo=serverless&logoColor=fff&style=for-the-badge" class="my-1" alt="ServerLess Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/AWS%20Lambda-F90?logo=awslambda&logoColor=fff&style=for-the-badge" class="my-1" alt="AWS Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Azure%20DevOps-0078D7?logo=azuredevops&logoColor=fff&style=for-the-badge" class="my-1" alt="Azure Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/IntelliJ%20IDEA-000?logo=intellijidea&logoColor=fff&style=for-the-badge" class="my-1" alt="InteliJ Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Visual%20Studio%20Code-007ACC?logo=visualstudiocode&logoColor=fff&style=for-the-badge" class="my-1" alt="VSCode Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Jira%20Software-0052CC?logo=jirasoftware&logoColor=fff&style=for-the-badge" class="my-1" alt="Jira Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Bitbucket-0052CC?logo=bitbucket&logoColor=fff&style=for-the-badge" class="my-1" alt="Bitbucket Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Confluence-172B4D?logo=confluence&logoColor=fff&style=for-the-badge" class="my-1" alt="Conflu Badge">
                      </div>
                      <div class="inline-flex mr-2">
                        <img src="https://img.shields.io/badge/Kibana-005571?logo=kibana&logoColor=fff&style=for-the-badge" class="my-1" alt="Kibana Badge">
                      </div>
                </div>
            </div>
            <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
                <p>Scroll to see more &rarr;</p>
            </div>
        </div>        
    </section>
</main>
