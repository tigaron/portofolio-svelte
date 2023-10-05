<script lang="ts">
	export let about: {
		name: string;
		description: string;
	};
	export let index: number;
</script>

<div class="flex gap-6 sm:gap-8">
	<div class="flex-none w-16 h-16">
		<p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
			0{index + 1}
		</p>
	</div>
	<div class="flex flex-col gap-6 sm:gap-8">
		<h3 class="text-2xl sm:text-3xl md:text-5xl">
			{about.name}
		</h3>
		<p>{about.description}</p>
	</div>
</div>
