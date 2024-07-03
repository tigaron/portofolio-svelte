<footer
	class="py-20 sm:py-32 bg-black border-t border-solid border-violet-950 flex flex-col gap-4 sm:gap-8 justify-center items-center"
>
	<p class="px-4 py-2 bg-white text-slate-950 font-medium">Connect with me &darr;</p>
	<div class="flex flex-col gap-4 items-center justify-center">
		<div class="flex items-center gap-4 sm:gap-6 text-2xl sm:text-3xl md:text-4xl mx-auto">
			<button on:click={() => window.open('mailto:suputra.iwn@gmail.com', '_blank')}>
				<i class="fa-regular fa-envelope" />
			</button>
			<button on:click={() => window.open('https://www.linkedin.com/in/nikesuputra/', '_blank')}>
				<i class="fa-brands fa-linkedin-in" />
			</button>
			<button on:click={() => window.open('https://github.com/tigaron/', '_blank')}>
				<i class="fa-brands fa-github" />
			</button>
		</div>
	</div>
</footer>
