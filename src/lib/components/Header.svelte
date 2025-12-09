<script lang="ts">
	import { ArrowUpRight } from 'lucide-svelte';
</script>

<header class="w-full px-4 md:px-8 py-6 flex items-center justify-between text-[10px] font-medium tracking-wide uppercase border-b border-transparent fixed top-0 left-0 z-50 bg-[#F4F4F2]/90 backdrop-blur-sm transition-all duration-300">
	<div class="flex-1">
		<a href="/" class="text-xl font-medium tracking-tighter">AVISION</a>
	</div>

	<nav class="hidden md:flex items-center gap-12 text-gray-500">
		<a href="#studio" class="hover:text-black transition-colors">Studio</a>
		<a href="#book" class="hover:text-black transition-colors">Book</a>
		<a href="#talents" class="hover:text-black transition-colors">Talents</a>
		<a href="#services" class="hover:text-black transition-colors">Services</a>
		<a href="#gallery" class="hover:text-black transition-colors">Gallery</a>
	</nav>

	<div class="flex-1 flex justify-end items-center gap-6 md:gap-8">
		<a href="#join" class="flex items-center gap-1 hover:opacity-70 transition-opacity">
			<ArrowUpRight size={14} />
			JOIN US
		</a>
		<a href="#contact" class="flex items-center gap-1 hover:opacity-70 transition-opacity">
			<ArrowUpRight size={14} />
			CONTACT
		</a>
	</div>
</header>
