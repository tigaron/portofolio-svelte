<script lang="ts">
	export let y: number;

	let tabs = [
		{ name: 'Projects', link: '#projects' },
		{ name: 'About Me', link: '#about' },
		{ name: 'Blog', link: 'https://www.youtube.com/watch?v=dQw4w9WgXcQ' }
	];
</script>

<header
	class={'sticky z-[10] top-0 duration-200 border-b border-solid ' +
		(y > 0 ? ' py-4 bg-slate-950 border-violet-950' : ' py-6 bg-transparent border-transparent')}
>
	<div class="container max-w-[1400px] px-6 mx-auto flex items-center justify-between">
		<h1 class="font-medium">
			<b class="font-bold poppins">Nike</b> Suputra
		</h1>
		<div class="sm:flex items-center gap-4 hidden">
			{#each tabs as tab, index}
				<a
					href={tab.link}
					class="duration-200 hover:text-violet-400"
					target={index === 2 ? '_blank' : ''}
				>
					<p>{tab.name}</p>
				</a>
			{/each}
			<button
				on:click={() => {
					window.open('mailto:suputra.iwn@gmail.com', '_blank');
				}}
				class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
			>
				<div
					class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
				/>
				<h4 class="relative z-9">Get in touch</h4>
			</button>
		</div>
	</div>
</header>
