<script lang="ts">
	import { linkedin, roles } from '#lib/content';

	const link =
		'underline decoration-2 underline-offset-[0.2em] transition-[text-decoration-color] duration-300';
</script>

<main>
	<header class="flex min-h-[88svh] flex-col bg-brand text-brand-ink">
		<div
			class="fade mx-auto flex w-full max-w-6xl items-baseline justify-between gap-4 px-4 pt-6 text-sm md:px-8 md:pt-8"
		>
			<p>Wilton, Connecticut</p>
			<a
				class="{link} decoration-brand-ink/40 hover:decoration-zap"
				href={linkedin}
				target="_blank"
				rel="noreferrer">LinkedIn ↗</a
			>
		</div>

		<div
			class="mx-auto mt-auto flex w-full max-w-6xl flex-col gap-8 px-4 pt-24 pb-10 md:flex-row md:items-end md:justify-between md:px-8 md:pb-16"
		>
			<h1 class="text-[clamp(3rem,12.5vw,6rem)] leading-[0.88] wide uppercase">
				<span class="block overflow-clip"><span class="rise">John</span></span>
				<span class="block overflow-clip"><span class="rise" style="--i: 1">Frisbee</span></span>
			</h1>
			<p class="fade max-w-[26ch] text-xl leading-snug md:text-right" style="--i: 3">
				Finance Director at The Robotics Catalyst Foundation. Senior at Wilton High School.
			</p>
		</div>
	</header>

	<section class="mx-auto max-w-6xl px-4 py-20 md:px-8 md:py-32">
		<p class="max-w-[38ch] text-2xl leading-snug md:text-[2rem]">
			I started a robotics foundation with other students in 2025 because I wanted it to exist. I
			ran its outreach for the first year and now look after its money.
		</p>

		<div class="mt-20 grid gap-y-6 md:mt-28 md:grid-cols-[14rem_1fr]">
			<h2 class="text-lg wide uppercase">Work</h2>
			<ol>
				{#each roles as role (role.title)}
					<li
						class="grid gap-x-8 gap-y-1 border-t border-ink py-6 first:border-t-2 md:grid-cols-[1fr_11rem]"
					>
						<div>
							<h3 class="text-xl font-semibold md:text-2xl">{role.title}</h3>
							<p class="text-mute">{role.org}</p>
							<p class="mt-3 max-w-[60ch]">{role.detail}</p>
						</div>
						<p class="order-first text-mute tabular-nums md:order-none md:text-right">
							{role.dates}
						</p>
					</li>
				{/each}
			</ol>

			<h2 class="mt-14 text-lg wide uppercase md:mt-20">School</h2>
			<div
				class="grid gap-x-8 gap-y-1 border-t-2 border-ink py-6 md:mt-20 md:grid-cols-[1fr_11rem]"
			>
				<div>
					<h3 class="text-xl font-semibold md:text-2xl">Wilton High School</h3>
					<p class="text-mute">Wilton, Connecticut</p>
				</div>
				<p class="order-first text-mute md:order-none md:text-right">Senior</p>
			</div>
		</div>
	</section>

	<footer class="bg-ink text-bg">
		<div class="mx-auto max-w-6xl px-4 pt-20 pb-8 md:px-8 md:pt-32">
			<h2 class="max-w-[22ch] text-2xl leading-snug md:text-[2rem]">
				Robotics, student organizations, or anything else, I’m happy to talk.
			</h2>
			<a
				class="wide {link} mt-8 inline-block text-[clamp(2.25rem,8vw,4.5rem)] leading-none uppercase decoration-brand hover:decoration-zap"
				href={linkedin}
				target="_blank"
				rel="noreferrer">LinkedIn ↗</a
			>
			<p class="mt-24 text-sm text-bg/60">© {new Date().getFullYear()} John Frisbee</p>
		</div>
	</footer>
</main>
