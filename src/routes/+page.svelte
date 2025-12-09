<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import { ArrowUpRight, ArrowRight } from 'lucide-svelte';

	const services = [
		{ id: '01', name: 'PHOTOGRAPHY' },
		{ id: '02', name: 'VIDEOGRAPHY' },
		{ id: '03', name: 'STYLIST' },
		{ id: '04', name: 'WEB DESIGN' },
		{ id: '05', name: 'GRAPHIC DESIGN' },
		{ id: '06', name: 'ILLUSTRATING' },
		{ id: '07', name: 'ART DIRECTION' }
	];

	const team = [
		{ name: 'KRISTEN SKINNER', role: 'PHOTOGRAPHER', img: 'https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=800&auto=format&fit=crop' },
		{ name: 'ADELE POTTS', role: 'VIDEOGRAPHER', img: 'https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?q=80&w=800&auto=format&fit=crop' },
		{ name: 'GARY HUBBARD', role: 'STYLIST', img: 'https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?q=80&w=800&auto=format&fit=crop' },
		{ name: 'LUISA OSBORN', role: 'WEB DESIGNER', img: 'https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=800&auto=format&fit=crop' },
		{ name: 'ANTIONE MATHIS', role: 'GRAPHIC DESIGNER', img: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?q=80&w=800&auto=format&fit=crop' },
		{ name: 'REBEKAH MAYER', role: 'ILLUSTRATOR', img: 'https://images.unsplash.com/photo-1438761681033-6461ffad8d80?q=80&w=800&auto=format&fit=crop' },
		{ name: 'LARRY FISHER', role: 'PHOTOGRAPHER', img: 'https://images.unsplash.com/photo-1500648767791-00dcc994a43e?q=80&w=800&auto=format&fit=crop' },
		{ name: 'CARMELA HERRERA', role: 'VIDEOGRAPHER', img: 'https://images.unsplash.com/photo-1517841905240-472988babdf9?q=80&w=800&auto=format&fit=crop' }
	];
</script>

<div class="min-h-screen bg-[#F4F4F2] text-[#1A1A1A] font-sans selection:bg-[#8B3A22] selection:text-white overflow-x-hidden">
	<Header />

	<main>
		<!-- Hero Section -->
		<section class="pt-12 md:pt-20 pb-10 px-4 md:px-8">
			<div class="flex flex-col md:flex-row justify-between items-start mb-12 md:mb-24 relative">
				<div class="max-w-[200px] text-[10px] leading-relaxed uppercase tracking-wide font-medium mt-2">
					<p>At Avision, we're more than just a creative agency; we're a dynamic platform dedicated to empowering talents.</p>
				</div>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right mt-8 md:mt-0 uppercase">
					Where <br />
					Creativity
				</h1>
			</div>

			<!-- Hero Images -->
			<div class="grid grid-cols-5 gap-2 md:gap-4 mb-8 h-[30vh] md:h-[50vh]">
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1620646233562-f2a31adcc8b6?q=80&w=800&auto=format&fit=crop" alt="Hands" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1618331835717-801e976710b2?q=80&w=800&auto=format&fit=crop" alt="Silhouette" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000 filter hue-rotate-180" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1570158268183-d296b2892211?q=80&w=800&auto=format&fit=crop" alt="Portrait" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=800&auto=format&fit=crop" alt="Mirror" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="https://images.unsplash.com/photo-1582201942988-13e60e4556ee?q=80&w=800&auto=format&fit=crop" alt="Art" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-start">
				<span class="text-[10px] uppercase tracking-wide font-medium mt-4 hidden md:block">Scroll</span>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right w-full uppercase">
					Meets <br />
					Opportunity
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
							Talents
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Team Section -->
		<section class="py-20 px-4 md:px-8 bg-[#F4F4F2]" id="talents">
			<div class="flex flex-col md:flex-row justify-between items-start mb-16 md:mb-24">
				<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-8 md:mb-0 uppercase">Avision Team</h2>
				<div class="max-w-xs text-[10px] leading-relaxed uppercase tracking-wide font-medium text-right md:text-left">
					<p>Our team consists of the most creative people from all over the world. For them, this is not just a job, it is what they live by.</p>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-12 md:gap-y-16">
				{#each team as member}
					<div class="group cursor-pointer">
						<div class="aspect-[3/4] overflow-hidden mb-4 bg-gray-200">
							<img src={member.img} alt={member.name} class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-500" />
						</div>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-1">{member.name}</h3>
						<p class="text-[10px] text-gray-500 uppercase tracking-wide mb-3">{member.role}</p>
						<div class="inline-flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity">
							<ArrowUpRight size={10} />
							Explore
						</div>
					</div>
				{/each}
				
				<!-- Join Us Card -->
				<div class="flex flex-col justify-between h-full min-h-[300px] border border-gray-300 p-8 bg-[#F4F4F2] hover:bg-white transition-colors cursor-pointer group">
					<div class="flex justify-center items-center flex-1">
						<ArrowRight size={48} class="text-gray-300 group-hover:text-black transition-colors" />
					</div>
					<div>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-1 leading-relaxed">We always welcome<br/>new talents!</h3>
						<div class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-4">
							<ArrowUpRight size={10} />
							Join Us
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- Studio Section -->
		<section class="py-20 px-4 md:px-8" id="studio">
			<div class="flex flex-col lg:flex-row mb-16 gap-12 lg:gap-24">
				<div class="flex-1">
					<h2 class="text-4xl md:text-6xl font-light tracking-tight uppercase">Avision Studio</h2>
				</div>
				<div class="flex-1">
					<h2 class="text-3xl md:text-5xl font-light tracking-tight mb-8 text-left uppercase leading-tight">The place where<br/>ideas are born</h2>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-[10px] leading-relaxed uppercase tracking-wide font-medium">
						<p>Avision is a creative agency dedicated to providing a platform for talented photographers, videographers & other talents to showcase their work and connect with clients.</p>
						<p>At Avision, we believe in the power of collaboration and are committed to providing a seamless and efficient process for both clients and team members. As a commission-based agency paid by clients, we offer a simple and transparent pricing structure that allows clients to view team member portfolios, get quotations, and book photography studio spaces, all through our automated systems and proper procedures.</p>
					</div>
					<a href="#about" class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-8 hover:opacity-60 transition-opacity">
						<ArrowUpRight size={10} />
						About
					</a>
				</div>
			</div>

			<div class="flex flex-col md:flex-row gap-4 h-[50vh] md:h-[70vh]">
				<div class="w-full md:w-[60%] h-full bg-gray-200 overflow-hidden">
					<img src="https://images.unsplash.com/photo-1596236560753-43f5ec316045?q=80&w=1200&auto=format&fit=crop" alt="Studio" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
				<div class="w-full md:w-[40%] h-full flex flex-col gap-4">
					<div class="flex-1 bg-gray-200 overflow-hidden">
						<img src="https://images.unsplash.com/photo-1513364776144-60967b0f800f?q=80&w=800&auto=format&fit=crop" alt="Studio Interior" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
					</div>
					<div class="flex-1 flex gap-4">
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?q=80&w=600&auto=format&fit=crop" alt="Studio Detail" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="https://images.unsplash.com/photo-1524758631624-e2822e304c36?q=80&w=600&auto=format&fit=crop" alt="Studio Detail" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- CTA Section -->
		<section class="py-32 px-4 md:px-8 bg-[#8B3A22] text-white text-center">
			<span class="text-[10px] font-medium uppercase tracking-widest mb-6 block opacity-80">Let's Create Together</span>
			<h2 class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mb-12 uppercase">
				We'd love to <br />
				work with you
			</h2>
			<a href="#contact" class="inline-block bg-[#1A1A1A] text-white px-10 py-4 rounded-full text-[10px] font-bold uppercase tracking-widest hover:bg-white hover:text-[#1A1A1A] transition-colors">
				Contact
			</a>
		</section>

		<!-- Bottom Gallery -->
		<div class="grid grid-cols-2 md:grid-cols-5 h-[60vh]">
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1515462277126-2dd0c162007a?q=80&w=800&auto=format&fit=crop" alt="Dancer" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1550614000-4b9519e0037a?q=80&w=800&auto=format&fit=crop" alt="Legs" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=800&auto=format&fit=crop" alt="Veil" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700 filter hue-rotate-90" />
			</div>
			<div class="overflow-hidden">
				<img src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?q=80&w=800&auto=format&fit=crop" alt="Pillows" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden hidden md:block">
				<img src="https://images.unsplash.com/photo-1595665593673-bf1ad72905c0?q=80&w=800&auto=format&fit=crop" alt="Red Dress" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
		</div>

		<!-- Footer Marquee -->
		<div class="overflow-hidden py-6 border-b border-gray-200">
			<div class="whitespace-nowrap animate-marquee flex">
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Creativity meets opportunity — Where creativity meets opportunity — Where creativity meets opportunity — </span>
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Creativity meets opportunity — Where creativity meets opportunity — Where creativity meets opportunity — </span>
			</div>
		</div>
	</main>

	<footer class="px-4 md:px-8 py-12 text-[10px] font-medium uppercase tracking-wide">
		<div class="flex flex-col md:flex-row justify-between items-start md:items-end gap-12 md:gap-8">
			<div class="flex flex-col gap-3">
				<a href="#studio" class="hover:opacity-60">Studio</a>
				<a href="#book" class="hover:opacity-60">Book</a>
				<a href="#talents" class="hover:opacity-60">Talents</a>
				<a href="#services" class="hover:opacity-60">Services</a>
				<a href="#gallery" class="hover:opacity-60">Gallery</a>
			</div>

			<div class="text-left md:text-center">
				<p class="text-xl md:text-3xl font-normal tracking-tight mb-2">+965 97315182</p>
				<p class="text-lg md:text-2xl font-normal tracking-tight mb-6">INFO@AVISIONKW.COM</p>
				<p class="text-lg tracking-widest">KUWAIT</p>
			</div>

			<div class="flex flex-col gap-3 text-left md:text-right">
				<a href="#privacy" class="hover:opacity-60">Privacy Policy</a>
				<a href="#terms" class="hover:opacity-60">Terms & Conditions</a>
			</div>
		</div>

		<div class="flex flex-col md:flex-row justify-between items-center mt-20 pt-8 border-t border-gray-200 text-[10px] text-gray-400 gap-4">
			<p>©AVISION STUDIO. ALL RIGHT RESERVRED</p>
			<div class="flex items-center gap-1">
				<span class="text-black text-lg font-bold tracking-tight">AVISION</span>
			</div>
			<p>DESIGNED BY VALMAX</p>
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

