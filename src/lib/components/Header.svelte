<script lang="ts">
	import { ArrowUpRight } from 'lucide-svelte';
</script>

<header class="w-full px-4 md:px-8 py-6 flex items-center justify-between text-[10px] font-medium tracking-wide uppercase border-b border-transparent fixed top-0 left-0 z-50 bg-[#F4F4F2]/90 backdrop-blur-sm transition-all duration-300">
	<div class="flex-1">
		<a href="/" class="block w-12 h-12 text-[#1A1A1A] hover:opacity-70 transition-opacity">
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 102 101" fill="none" class="w-full h-full">
				<path d="M0.464844 100.557H25.6042L0.464844 0V100.557Z" fill="currentColor"/>
				<path d="M50.7437 100.557H75.883L50.7437 0V100.557Z" fill="currentColor"/>
				<path d="M25.604 100.557H50.7434L25.604 0V100.557Z" fill="currentColor"/>
				<path d="M75.8828 100.557H101.022L75.8828 0V100.557Z" fill="currentColor"/>
			</svg>
		</a>
	</div>

	<nav class="hidden md:flex items-center gap-12 text-gray-500">
		<a href="#about" class="hover:text-black transition-colors">About</a>
		<a href="#services" class="hover:text-black transition-colors">Services</a>
		<a href="#packages" class="hover:text-black transition-colors">Packages</a>
		<a href="#equipment" class="hover:text-black transition-colors">Equipment</a>
	</nav>

	<div class="flex-1 flex justify-end items-center gap-6 md:gap-8">
		<a href="#book" class="flex items-center gap-1 hover:opacity-70 transition-opacity">
			<ArrowUpRight size={14} />
			BOOK NOW
		</a>
		<a href="#contact" class="flex items-center gap-1 hover:opacity-70 transition-opacity">
			<ArrowUpRight size={14} />
			CONTACT
		</a>
	</div>
</header>
