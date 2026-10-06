<script lang="ts">
	import { linkedin, roles } from '#lib/content';
</script>

<main id="top">
	<section class="relative overflow-hidden border-b border-line">
		<div
			class="pointer-events-none absolute inset-0 opacity-[0.18]"
			style="background-image: linear-gradient(var(--color-line) 1px, transparent 1px), linear-gradient(90deg, var(--color-line) 1px, transparent 1px); background-size: 48px 48px;"
		></div>
		<div class="relative mx-auto grid max-w-6xl gap-12 px-5 py-20 md:grid-cols-[1.2fr_0.8fr] md:px-8 md:py-28">
			<div>
				<p class="font-mono text-xs tracking-[0.22em] text-leaf uppercase">
					Wilton Center, Connecticut
				</p>
				<h1 class="mt-4 font-display text-[clamp(3.2rem,9vw,7rem)] leading-[0.9] tracking-tight">
					John
					<br />
					Frisbee
				</h1>
				<p class="mt-8 max-w-xl text-lg leading-relaxed text-mute">
					Founder and Finance Director at The Robotics Catalyst Foundation. Senior at Wilton High
					School.
				</p>
				<div class="mt-10 flex flex-wrap gap-3">
					<a
						class="rounded-full bg-forest px-5 py-2.5 text-sm font-medium text-paper hover:bg-leaf"
						href="#work"
					>
						See the work
					</a>
					<a
						class="rounded-full border border-ink/20 px-5 py-2.5 text-sm font-medium hover:border-ink"
						href={linkedin}
						target="_blank"
						rel="noreferrer"
					>
						View LinkedIn
					</a>
				</div>
			</div>
			<aside class="self-end rounded-3xl border border-line bg-paper-2 p-8">
				<p class="font-mono text-xs tracking-[0.18em] text-mute uppercase">Now</p>
				<p class="mt-4 font-display text-3xl leading-tight">The Robotics Catalyst Foundation</p>
				<p class="mt-3 text-mute">
					Student-founded organization. Finance Director since November 2025, after founding the
					group and leading outreach.
				</p>
			</aside>
		</div>
	</section>

	<section id="about" class="mx-auto max-w-6xl px-5 py-20 md:px-8">
		<div class="grid gap-10 md:grid-cols-12">
			<h2 class="font-mono text-xs tracking-[0.22em] text-leaf uppercase md:col-span-3">About</h2>
			<div class="max-w-2xl space-y-5 text-lg leading-relaxed md:col-span-9">
				<p>
					I am a senior at Wilton High School building something I wanted to exist: a foundation
					that treats robotics as a catalyst, not just a club.
				</p>
				<p class="text-mute">
					The Robotics Catalyst Foundation is where I have spent the last year and a half —
					starting as Founder and Head of Outreach, then stepping into Finance Director. The work
					sits at the intersection of student leadership, community, and making robotics reachable.
				</p>
			</div>
		</div>
	</section>

	<section id="work" class="border-y border-line bg-paper-2/60">
		<div class="mx-auto max-w-6xl px-5 py-20 md:px-8">
			<div class="mb-12 flex items-end justify-between gap-6">
				<div>
					<p class="font-mono text-xs tracking-[0.22em] text-leaf uppercase">Experience</p>
					<h2 class="mt-2 font-display text-4xl md:text-5xl">The work so far</h2>
				</div>
				<p class="hidden max-w-xs text-sm text-mute md:block">
					One organization, two hats: first outreach, now finance.
				</p>
			</div>
			<ol class="space-y-6">
				{#each roles as role, i}
					<li class="rounded-2xl border border-line bg-paper p-6 md:p-8">
						<div class="flex flex-wrap items-baseline justify-between gap-3">
							<p class="font-mono text-xs text-mute">0{i + 1}</p>
							<p class="font-mono text-xs text-mute">{role.dates}</p>
						</div>
						<h3 class="mt-4 font-display text-2xl md:text-3xl">{role.title}</h3>
						<p class="mt-1 text-leaf">{role.org} · {role.type}</p>
						<p class="mt-4 max-w-2xl text-mute">{role.detail}</p>
					</li>
				{/each}
			</ol>
		</div>
	</section>

	<section id="education" class="mx-auto max-w-6xl px-5 py-20 md:px-8">
		<div class="grid gap-10 md:grid-cols-12">
			<h2 class="font-mono text-xs tracking-[0.22em] text-leaf uppercase md:col-span-3">
				Education
			</h2>
			<div class="rounded-2xl border border-line p-8 md:col-span-9">
				<p class="font-display text-3xl">Wilton High School</p>
				<p class="mt-2 text-mute">Wilton Center, Connecticut · Grade: Senior</p>
				<p class="mt-6 max-w-xl text-mute">
					Alongside school, I founded and run The Robotics Catalyst Foundation — a live test of
					leadership, operations, and follow-through.
				</p>
			</div>
		</div>
	</section>

	<section id="contact" class="border-t border-line bg-forest text-paper">
		<div class="mx-auto max-w-6xl px-5 py-20 md:px-8">
			<p class="font-mono text-xs tracking-[0.22em] text-moss uppercase">Contact</p>
			<h2 class="mt-4 max-w-2xl font-display text-4xl leading-tight md:text-6xl">
				Let’s talk robotics, student orgs, or what comes next.
			</h2>
			<a
				class="mt-10 inline-flex rounded-full bg-paper px-6 py-3 font-medium text-forest hover:bg-paper-2"
				href={linkedin}
				target="_blank"
				rel="noreferrer"
			>
				Connect on LinkedIn
			</a>
		</div>
	</section>
</main>
