<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import { ArrowUpRight, ArrowRight } from 'lucide-svelte';

	const services = [
		{ id: '01', name: 'LIVE MIXING' },
		{ id: '02', name: 'MASTER OF CEREMONIES' },
		{ id: '03', name: 'SOUND REINFORCEMENT' },
		{ id: '04', name: 'LIGHTING DESIGN' },
		{ id: '05', name: 'WIRELESS MICROPHONES' },
		{ id: '06', name: 'CUSTOM DJ BOOTH' },
		{ id: '07', name: 'RECORDED LIVE SETS' }
	];

	const packages = [
		{ name: 'WEDDINGS', description: 'Modern, non-cheesy musical backdrop for your big day', img: 'https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=800&auto=format&fit=crop' },
		{ name: 'CORPORATE EVENTS', description: 'Clean, upbeat, brand-safe entertainment', img: 'https://images.unsplash.com/photo-1511578314322-379afb476865?q=80&w=800&auto=format&fit=crop' },
		{ name: 'PRIVATE VIP FUNCTIONS', description: 'Discretion and tailored musical atmosphere', img: 'https://images.unsplash.com/photo-1464366400600-7168b8af9bc3?q=80&w=800&auto=format&fit=crop' },
		{ name: 'NIGHTLIFE VENUES', description: 'High-energy talent to keep patrons engaged', img: 'https://images.unsplash.com/photo-1566737236500-c8ac43014a67?q=80&w=800&auto=format&fit=crop' }
	];
</script>

<div class="min-h-screen bg-[#F4F4F2] text-[#1A1A1A] font-sans selection:bg-[#8B3A22] selection:text-white overflow-x-hidden">
	<Header />

	<main>
		<!-- Hero Section -->
		<section class="pt-12 md:pt-20 pb-10 px-4 md:px-8">
			<div class="flex flex-col md:flex-row justify-between items-start mb-12 md:mb-24 relative">
				<div class="max-w-[200px] text-[10px] leading-relaxed uppercase tracking-wide font-medium mt-2">
					<p>We don't just play music; we provide a full-scale audio-visual production tailored to the venue.</p>
				</div>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right mt-8 md:mt-0 uppercase">
					Where <br />
					Energy
				</h1>
			</div>

			<!-- Hero Images -->
			<div class="grid grid-cols-5 gap-2 md:gap-4 mb-8 h-[30vh] md:h-[50vh]">
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1470225620780-dba8ba36b745?q=80&w=800&auto=format&fit=crop" alt="DJ Equipment" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1516450360452-9312f5e86fc7?q=80&w=800&auto=format&fit=crop" alt="Concert Crowd" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1571266028243-d220c6e87a67?q=80&w=800&auto=format&fit=crop" alt="DJ Mixing" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1514525253161-7a46d19cd819?q=80&w=800&auto=format&fit=crop" alt="Event Lighting" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1492684223066-81342ee5ff30?q=80&w=800&auto=format&fit=crop" alt="Wedding Reception" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-start">
				<span class="text-[10px] uppercase tracking-wide font-medium mt-4 hidden md:block">Scroll</span>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right w-full uppercase">
					Meets <br />
					Experience
				</h1>
			</div>
		</section>

		<!-- Services Section -->
		<section class="py-20 md:py-32" id="services">
			<div class="flex justify-center mb-16 md:mb-24">
				<span class="text-[10px] font-bold uppercase tracking-widest">Services</span>
			</div>

			<div class="border-t border-gray-300">
				{#each services as service}
					<div class="group border-b border-gray-300 py-6 md:py-10 px-4 md:px-8 flex items-center justify-between hover:bg-white transition-colors cursor-pointer">
						<span class="text-[10px] font-medium text-gray-500 w-8 md:w-12">/{service.id}</span>
						<h2 class="text-3xl md:text-6xl lg:text-7xl font-thin tracking-tight group-hover:italic transition-all duration-300 uppercase">{service.name}</h2>
						<div class="flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity translate-x-[-10px] group-hover:translate-x-0 duration-300">
							<ArrowUpRight size={12} />
							Details
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- About & Packages Section -->
		<section class="py-20 px-4 md:px-8 bg-[#F4F4F2]" id="about">
			<div class="flex flex-col md:flex-row justify-between items-start mb-16 md:mb-24">
				<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-8 md:mb-0 uppercase">The Oren Advantage</h2>
				<div class="max-w-xs text-[10px] leading-relaxed uppercase tracking-wide font-medium text-right md:text-left">
					<p>In a market saturated with generic playlist DJs, DJ Oren stands out through technical skill and adaptability.</p>
				</div>
			</div>

			<!-- About DJ Oren -->
			<div class="mb-20 grid grid-cols-1 lg:grid-cols-2 gap-8 md:gap-12">
				<div class="aspect-[4/5] overflow-hidden bg-gray-200">
					<img src="https://images.unsplash.com/photo-1571266028243-d220c6e87a67?q=80&w=1200&auto=format&fit=crop" alt="DJ Oren" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
				<div class="flex flex-col justify-center gap-8">
					<div>
						<h3 class="text-2xl md:text-4xl font-light tracking-tight mb-4 uppercase">Open-Format Mastery</h3>
						<p class="text-[10px] leading-relaxed uppercase tracking-wide font-medium">The ability to switch genres instantly based on real-time crowd reaction, rather than sticking to a rigid setlist.</p>
					</div>
					<div>
						<h3 class="text-2xl md:text-4xl font-light tracking-tight mb-4 uppercase">Professionalism</h3>
						<p class="text-[10px] leading-relaxed uppercase tracking-wide font-medium">We treat DJing as a business—this means prompt communication, iron-clad contracts, and punctuality.</p>
					</div>
					<div>
						<h3 class="text-2xl md:text-4xl font-light tracking-tight mb-4 uppercase">Modern Vibe</h3>
						<p class="text-[10px] leading-relaxed uppercase tracking-wide font-medium">We avoid the clichés in favor of a club-inspired, high-energy mixing style that appeals to modern audiences.</p>
					</div>
				</div>
			</div>

			<!-- Packages -->
			<div class="mb-12">
				<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-12 uppercase text-center" id="packages">Booking & Packages</h2>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 gap-x-4 gap-y-12 md:gap-y-16">
				{#each packages as pkg}
					<div class="group cursor-pointer">
						<div class="aspect-[16/9] overflow-hidden mb-4 bg-gray-200">
							<img src={pkg.img} alt={pkg.name} class="w-full h-full object-cover group-hover:scale-105 transition-all duration-500" />
						</div>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-1">{pkg.name}</h3>
						<p class="text-[10px] text-gray-500 uppercase tracking-wide mb-3">{pkg.description}</p>
						<div class="inline-flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity">
							<ArrowUpRight size={10} />
							Learn More
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Equipment Section -->
		<section class="py-20 px-4 md:px-8" id="equipment">
			<div class="flex flex-col lg:flex-row mb-16 gap-12 lg:gap-24">
				<div class="flex-1">
					<h2 class="text-4xl md:text-6xl font-light tracking-tight uppercase">Experience & Equipment</h2>
				</div>
				<div class="flex-1">
					<h2 class="text-3xl md:text-5xl font-light tracking-tight mb-8 text-left uppercase leading-tight">Full-scale audio-visual<br/>production</h2>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-[10px] leading-relaxed uppercase tracking-wide font-medium">
						<p>Top-tier PA systems from QSC and JBL suitable for crowds from 50 to 500+. Intelligent moving heads, uplighting for ambiance, and dance floor wash lighting create the perfect atmosphere.</p>
						<p>At the core of the operation is DJ Oren, an open-format selector specializing in reading crowds and seamlessly blending genres to keep the energy high. Supported by a dedicated logistics crew for setup and breakdown, ensuring every event is technically flawless and musically unforgettable.</p>
					</div>
					<a href="#book" class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-8 hover:opacity-60 transition-opacity">
						<ArrowUpRight size={10} />
						Book Now
					</a>
				</div>
			</div>

			<div class="flex flex-col md:flex-row gap-4 h-[50vh] md:h-[70vh]">
				<div class="w-full md:w-[60%] h-full bg-gray-200 overflow-hidden">
					<img src="https://images.unsplash.com/photo-1598387993441-a364f854c3e1?q=80&w=1200&auto=format&fit=crop" alt="DJ Equipment Setup" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
				<div class="w-full md:w-[40%] h-full flex flex-col gap-4">
					<div class="flex-1 bg-gray-200 overflow-hidden">
						<img src="https://images.unsplash.com/photo-1563841930606-67e2bce48b78?q=80&w=800&auto=format&fit=crop" alt="Sound System" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
					</div>
					<div class="flex-1 flex gap-4">
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="https://images.unsplash.com/photo-1511379938547-c1f69419868d?q=80&w=600&auto=format&fit=crop" alt="Lighting Equipment" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="https://images.unsplash.com/photo-1571266028243-d220c6e87a67?q=80&w=600&auto=format&fit=crop" alt="DJ Mixing Console" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- CTA Section -->
		<section class="py-32 px-4 md:px-8 bg-[#8B3A22] text-white text-center" id="book">
			<span class="text-[10px] font-medium uppercase tracking-widest mb-6 block opacity-80">Ready to Elevate Your Event?</span>
			<h2 class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mb-12 uppercase">
				Let's make your <br />
				event unforgettable
			</h2>
			<a href="#contact" class="inline-block bg-[#1A1A1A] text-white px-10 py-4 rounded-full text-[10px] font-bold uppercase tracking-widest hover:bg-white hover:text-[#1A1A1A] transition-colors">
				Book Now
			</a>
		</section>

		<!-- Bottom Gallery -->
		<div class="grid grid-cols-2 md:grid-cols-5 h-[60vh]">
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1429962714451-bb934ecdc4ec?q=80&w=800&auto=format&fit=crop" alt="Wedding Dance Floor" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1540039155733-5bb30b53aa14?q=80&w=800&auto=format&fit=crop" alt="Corporate Event" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1470229722913-7c0e2dbbafd3?q=80&w=800&auto=format&fit=crop" alt="DJ Performance" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1519167758481-83f29da8c2b7?q=80&w=800&auto=format&fit=crop" alt="Event Crowd" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden hidden md:block">
				<img src="https://images.unsplash.com/photo-1516450360452-9312f5e86fc7?q=80&w=800&auto=format&fit=crop" alt="Concert Atmosphere" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
		</div>

		<!-- Footer Marquee -->
		<div class="overflow-hidden py-6 border-b border-gray-200">
			<div class="whitespace-nowrap animate-marquee flex">
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Where energy meets experience — Where energy meets experience — Where energy meets experience — </span>
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Where energy meets experience — Where energy meets experience — Where energy meets experience — </span>
			</div>
		</div>
	</main>

	<footer class="px-4 md:px-8 py-12 text-[10px] font-medium uppercase tracking-wide" id="contact">
		<div class="flex flex-col md:flex-row justify-between items-start md:items-end gap-12 md:gap-8">
			<div class="flex flex-col gap-3">
				<a href="#about" class="hover:opacity-60">About</a>
				<a href="#services" class="hover:opacity-60">Services</a>
				<a href="#packages" class="hover:opacity-60">Packages</a>
				<a href="#equipment" class="hover:opacity-60">Equipment</a>
				<a href="#book" class="hover:opacity-60">Book Now</a>
			</div>

			<div class="text-left md:text-center">
				<p class="text-xl md:text-3xl font-normal tracking-tight mb-2">+1 (555) 123-4567</p>
				<p class="text-lg md:text-2xl font-normal tracking-tight mb-6">BOOKING@DJOREN.COM</p>
				<p class="text-lg tracking-widest">AVAILABLE NATIONWIDE</p>
			</div>

			<div class="flex flex-col gap-3 text-left md:text-right">
				<a href="#privacy" class="hover:opacity-60">Privacy Policy</a>
				<a href="#terms" class="hover:opacity-60">Terms & Conditions</a>
			</div>
		</div>

		<div class="flex flex-col md:flex-row justify-between items-center mt-20 pt-8 border-t border-gray-200 text-[10px] text-gray-400 gap-4">
			<p>©DJ OREN. ALL RIGHTS RESERVED</p>
			<div class="flex items-center gap-1">
				<div class="w-8 h-8 text-[#1A1A1A]">
					<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 102 101" fill="none" class="w-full h-full">
						<path d="M0.464844 100.557H25.6042L0.464844 0V100.557Z" fill="currentColor"/>
						<path d="M50.7437 100.557H75.883L50.7437 0V100.557Z" fill="currentColor"/>
						<path d="M25.604 100.557H50.7434L25.604 0V100.557Z" fill="currentColor"/>
						<path d="M75.8828 100.557H101.022L75.8828 0V100.557Z" fill="currentColor"/>
					</svg>
				</div>
			</div>
			<p>PROFESSIONAL DJ SERVICES</p>
		</div>
	</footer>
</div>

<style>
	@keyframes marquee {
		0% { transform: translateX(0); }
		100% { transform: translateX(-50%); }
	}
	.animate-marquee {
		animation: marquee 30s linear infinite;
	}
</style>

