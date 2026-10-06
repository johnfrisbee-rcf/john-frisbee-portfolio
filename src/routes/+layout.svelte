<script lang="ts">
	import './layout.css';
	import favicon from '#lib/assets/favicon.svg';
	import type { LayoutProps } from './$types';
	import { linkedin } from '#lib/content';

	let { children }: LayoutProps = $props();

	const links = [
		{ href: '#work', label: 'Work' },
		{ href: '#education', label: 'Education' },
		{ href: '#contact', label: 'Contact' }
	];

	let open = $state(false);
</script>

<svelte:head>
	<title>John Frisbee</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="min-h-dvh bg-paper text-ink">
	<header
		class="sticky top-0 z-40 border-b border-line/80 bg-paper/90 backdrop-blur-md"
	>
		<div class="mx-auto flex max-w-6xl items-center justify-between px-5 py-4 md:px-8">
			<a href="#top" class="font-display text-xl tracking-tight">John Frisbee</a>
			<nav class="hidden items-center gap-8 md:flex" aria-label="Primary">
				{#each links as link}
					<a class="text-sm text-mute transition hover:text-ink" href={link.href}>{link.label}</a>
				{/each}
				<a
					class="rounded-full bg-forest px-4 py-2 text-sm font-medium text-paper transition hover:bg-leaf"
					href={linkedin}
					target="_blank"
					rel="noreferrer"
				>
					LinkedIn
				</a>
			</nav>
			<button
				class="rounded-md border border-line px-3 py-1.5 text-sm md:hidden"
				aria-expanded={open}
				aria-controls="mobile-nav"
				onclick={() => (open = !open)}
			>
				{open ? 'Close' : 'Menu'}
			</button>
		</div>
		{#if open}
			<nav
				id="mobile-nav"
				class="flex flex-col gap-3 border-t border-line px-5 py-4 md:hidden"
				aria-label="Mobile"
			>
				{#each links as link}
					<a href={link.href} onclick={() => (open = false)}>{link.label}</a>
				{/each}
				<a href={linkedin} target="_blank" rel="noreferrer">LinkedIn</a>
			</nav>
		{/if}
	</header>

	{@render children()}

	<footer class="border-t border-line px-5 py-10 md:px-8">
		<div class="mx-auto flex max-w-6xl flex-col gap-2 text-sm text-mute md:flex-row md:justify-between">
			<p>© {new Date().getFullYear()} John Frisbee</p>
			<p>Wilton Center, Connecticut</p>
		</div>
	</footer>
</div>
