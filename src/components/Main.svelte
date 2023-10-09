<script lang="ts">
	import Step from '../components/Step.svelte';
	import About from './About.svelte';

	let steps = [
		{
			name: 'T-Shirt Store - CMS',
			icon: 'fa-solid fa-cart-shopping',
			href: 'https://store-admin.fourleaves.studio/',
			content:
				'<p>T-Shirt Store CMS is a simple e-commerce store dashboard and content management system created with <strong class="text-violet-400">Next.js, TailwindCSS, Prisma, MySQL, and Stripe API!</strong> Stripe API is used to allow for secure checkouts and handle all transactions. To login, use email "<em>test@fourleaves.studio</em>" and password "<em>password</em>".</p>'
		},
		{
			name: 'T-Shirt Store',
			icon: 'fa-solid fa-cart-shopping',
			href: 'https://store-front.fourleaves.studio/',
			content:
				'<p>T-Shirt Store is a simple e-commerce store frontend created with <strong class="text-violet-400">Next.js and TailwindCSS!</strong> It consumes data from T-Shirt Store - CMS APIs.</p>'
		},
		{
			name: 'Ultimate Todos',
			icon: 'fa-solid fa-list-check',
			href: '#todos',
			content:
				'<p>Ultimate Todos is a Full Stack <strong class="text-violet-400">Sveltekit and Firebase</strong> CRUD application that allows a user to login, manage a tidy and efficacious todo list, and persist this information across devices.</p>'
		},
	];

	let abouts = [
		{
			name: 'a self taught developer',
			description:
				"I started learning to code through online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. I began with the fundamentals, building simple websites with JavaScript, HTML, and CSS. As my skills grew, I delved into backend development, honing my expertise with technologies like Node.js + Express.js and Go + Gin."
		},
		{
			name: 'a cloud devops enthusiast',
			description:
				"Embracing the dynamic world of cloud DevOps, I am driven by a relentless passion for optimizing and automating the development and deployment process. Currently, I'm actively exploring Amazon Web Services (AWS) to expand my proficiency in cloud-based DevOps practices. I immersed myself in learning the ins and outs of cloud computing, infrastructure as code (IaC), and continuous integration/continuous deployment (CI/CD) pipelines."
		},
		{
			name: 'a collaborative problem solver',
			description:
				"Throughout my journey as a self-taught developer and cloud DevOps enthusiast, I've come to value not only technical expertise but also the power of collaboration. As a collaborative problem solver, I thrive in team environments where collective innovation and problem-solving are essential. I believe that diverse perspectives and skill sets are the driving force behind successful projects. My ability to communicate effectively, listen actively, and adapt to different viewpoints allows me to bridge gaps and forge connections within cross-functional teams."
		}
	];
</script>

<main class="container max-w-[1400px] mx-auto flex flex-col flex-1 p-4">
	<section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
		<div
			class="flex flex-col lg:justify-center text-center lg:text-left gap-2 md:gap-4 lg:gap-6 order-first lg:order-last"
		>
			<h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
				Hi! I'm <span class="poppins text-violet-400">Nike</span> Suputra
				<br />Software <span class="poppins text-violet-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				I'm a passionate software developer with a knack for solving complex problems and a love for
				clean, efficient code. With over 3 years of experience, I've delivered impactful solutions
				using <span class="text-violet-400">JavaScript, TypeScript, and Go</span>.
			</p>
			<p class="text-base sm:text-lg md:text-xl">
				My expertise spans from crafting responsive front-end interfaces to optimizing
				high-performance back-end systems. I thrive on collaborating with cross-functional teams to
				turn innovative ideas into reality.
			</p>
			<p class="text-base sm:text-lg md:text-xl">
				Let's connect and discuss how we can drive innovation together.
			</p>
			<button
				on:click={() => {
					window.open('mailto:suputra.iwn@gmail.com', '_blank');
				}}
				class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
			>
				<div
					class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
				/>
				<h4 class="relative z-9">Get in touch &rarr;</h4>
			</button>
		</div>
		<div class="relative shadow-2xl grid place-items-center order-last lg:order-first">
			<img src={'images/Profile.jpg'} alt="Nike Suputra" class="object-cover z-[2] max-h-[70vh] rounded-lg" />
		</div>
	</section>
	<section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-large sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				Curious to <span class="poppins text-violet-400">see</span> my work?
			</h3>
		</div>
		<div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
			{#each steps as step}
				<Step {step} />
			{/each}
		</div>
	</section>
	<section
		id="about"
		class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
	>
		<div
			class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
		>
			<h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me.
			</h3>
		</div>
		<p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
		<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
			{#each abouts as about, index}
				<About {about} {index} />
			{/each}
		</div>
	</section>
</main>
