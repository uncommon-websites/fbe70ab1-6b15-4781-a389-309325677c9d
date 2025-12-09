<script lang="ts">
	import "../app.css";
	import { onMount } from 'svelte';

	// Load Inter font
	onMount(() => {
		const link = document.createElement('link');
		link.href = 'https://fonts.googleapis.com/css2?family=Inter:wght@200;300;400;500;600&display=swap';
		link.rel = 'stylesheet';
		document.head.appendChild(link);
	});
</script>

<slot />
