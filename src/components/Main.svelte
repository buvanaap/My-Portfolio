<script>
    import Step from './Step.svelte'
    let steps=[
        {name:'Basic Banking System',icon:'fa-solid fa-building-columns'},
        {name:'Twisted Search',icon:'fa-brands fa-searchengin'},
        {name:'Employee Management System',icon:'fa-solid fa-bars-progress'},
    ]
    let benefits=[{name:'A self taught developer',description:'I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, and much much more.'},
    {name:'An excellent communicator',description:'Communication is key and its a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.'}
    ]
    const resumeFile = "/documents/Buvanaa-Resume .pdf";

</script>

<main class="flex flex-col flex-1 p-4">
   <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
       <div class="flex flex-col lg:justify-content text-center lg:text-left gap-6 md:gap-8 lg:gap=10">
        <h2 class="font-semibold text-4xl sa:text-5xl md:text-6xl">
            Hi! I'm
            <span class="poppins text-violet-400">Buvanaa </span> <br/>MERN Full Stack <span class="poppins text-violet-400">Developer</span>
        </h2>
        <p class="text-base sa:text-lg md:text-xl">
            My <span class="text-violet-400">favourite tech</span> includes JavaScript(Node.Js or SvelteKit),React.js,Express.js,MongoDb!
        </p>
        <a href="#" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 ">
            <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
            <h4 class="relative z-9">Get in Touch &rarr;</h4>
        </a>
       </div>
      <!-- <div class="relative shadow-2xl grid place-item-center">
        <img src={"images/profile.png.jpeg"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]"/>
       </div> --!>

   </section>
   <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
        <h6 class="text-larger sm:text-xl md:text-2xl">A few of my creative endevors</h6>
        <h3>Curious to <span class="poppins text-violet-400">see</span>my work?</h3>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        <Step step={steps[0]}>
              <p> A web application used to tranfer virtual money between multiple users and also record the banking transactions/ activities.</p> 
        </Step>
        <Step step={steps[1]}>
              <p>Twisted Search is a web app that redirects your search query to Google with the word "opossum" appended. The app is built using a custom prompt from Google AI Studio and uses Docker to run the code locally.</p>
        </Step>
        <Step step={steps[2]}>
            <p>The Employee Management System is a powerful and user-friendly application designed to streamline HR operations. It provides essential functionalities such as viewing, adding, updating, and deleting employee records, helping organizations manage their workforce efficiently.</p>
        </Step>
    </div>
   
   </section>
   <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
     after:absolute after:bottom-0 after:right-0 after:h-1.5 after:w-2/3 after:bg-violet-700 py-4">
     
     <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
     <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-violet-400">about</span>me.</h3>
    </div>
      <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am...</p>
      <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each benefits as benefit,index}
        <div class="flex gap-6 sm:gap-8">
            <p class="poppins text-4xl sm:text-5xl md:text6xl text-slate-500 font-semibold">
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
      <div class="flex flex-col items-center gap-8 max-w-[800px] mx-auto w-full py-10">
        <h3 class="text-3xl font-bold text-center">
            My <span class="text-violet-400">Resume</span>
        </h3>
        <p class="text-lg text-center">
            Curious about my journey? 💬 Explore my experience, skills, and projects in detail.<br>
            Feel free to <span class="font-bold">view</span> or <span class="font-bold">download</span> my resume below! 😊
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center w-full">
            <a 
                href={resumeFile} 
                download 
                class="bg-violet-500 hover:bg-violet-600 text-white font-bold py-3 px-6 rounded-lg transition-colors flex items-center gap-2"
            >
                <i class="fa-solid fa-download"></i>
                Download Resume
            </a>
            
            <a 
                href={resumeFile} 
                target="_blank" 
                class="bg-gray-100 hover:bg-gray-200 text-gray-800 font-bold py-3 px-6 rounded-lg transition-colors flex items-center gap-2"
            >
                <i class="fa-solid fa-eye"></i>
                View Resume
            </a>
        </div>
      </div>
      <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
        <p>Scroll to see more &rarr;</p>
      </div>

      <p class="mx-auto">So why not invest?</p>
   </section>
</main>
