<script>
	import { slide } from 'svelte/transition';
	import Icon from './lib/Icon.svelte';
	import profilePhoto from './assets/arsalan.jpg';

	let openSections = $state({});

	function toggle(id) {
		openSections = { ...openSections, [id]: !openSections[id] };
	}
</script>

<svelte:head>
	<title>Arsalan Bin Najeeb Wyne</title>
	<meta name="description" content="My personal timeline hosted, and also all of my thinking" />
</svelte:head>

<main class="page">
	<header class="profile d-flex justify-content-center ml-2">
		<img src={profilePhoto} alt="Arsalan Bin Najeeb Wyne" />
		<div class="d-flex align-items-center m-4 profile-name">
			<span>Arsalan Bin Najeeb Wyne</span>
		</div>
	</header>

	<div class="m-4">
		<div class="card">
			<div class="card-body">
				<p class="card-text d-inline-block">
					<a class="d-inline-block mx-4" href="mailto:arsalannajeeb0@gmail.com"
						><Icon name="mailbox" class="mr-2" />arsalannajeeb0</a
					>
					<a class="d-inline-block mx-4" href="https://github.com/anw10"
						><Icon name="github" class="mr-2" />anw10</a
					>
					<a class="d-inline-block mx-4" href="https://www.linkedin.com/in/arsalanwyne/"
						><Icon name="linkedin" class="mr-2" />arsalanwyne</a
					>
				</p>
			</div>
		</div>
		<div class="card mt-2">
			<div class="card-body">
				<h4 class="card-title">About Me</h4>
				<p class="card-text d-inline-block">
					I am pursuing my PhD @ George Washington University under Professor Jie Zhou. I also like
					to hike. <span>&#127802;</span>
				</p>
			</div>
		</div>
	</div>

	<section class="page-section">
		<div class="section-heading d-flex justify-content-between mx-4">
			<h2 class="align-self-center">Research</h2>
			<button
				class="toggle-button clickable"
				aria-label="Toggle Research"
				aria-expanded={!!openSections.research}
				onclick={() => toggle('research')}
			>
				<Icon name="patch-plus" class="section-icon icon-spin" />
			</button>
		</div>
		{#if openSections.research}
			<div class="section-content mt-2" transition:slide={{ duration: 250 }}>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Rust Benchmarking</h4>
						<p class="card-text d-inline-block">
							In progress research project to create a universal benchmarking tool for Safe &amp;
							Unsafe Rust. Achieved by developing custom LLVM passes, static and dynamic analysis of
							rust programs and instrumenting the rust compiler. The goal is to create a tool that
							can be used to benchmark Rust code and provide insights into its performance while
							also highlighting the importance and usage of unsafe rust.
						</p>
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Weak to Strong Alignment</h4>
						<p class="card-text d-inline-block">
							Implemented and investigated the affects of Weak to Strong Alignment by using BERT and
							GPT-4o. Presented my findings at GWU through their AI special topics platform. Also
							evaluated the consequences of using Weak to Strong Alignment on the safety of the
							final Strong model by running tests on the SST2 benchmark.
						</p>
						<a
							class="btn btn-outline-dark"
							style="color: purple; border-color: purple; background-color: white"
							href="https://github.com/anw10/W2S_Safety">Open Repo</a
						>
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">South Asian Computing</h4>
						<p class="card-text d-inline-block">
							My co-authored publication for ICER 2020 investigates the enacted computing curriculum
							and its various side affects for South Asian's. We gathered and compiled data relating
							to CS-ED and where the curriculum currently stands for countries that have little to
							none representation from Asia as a whole and more specifically South Asia.
						</p>
						<a
							class="btn btn-outline-dark"
							style="color: purple; border-color: purple; background-color: white"
							href="https://dl.acm.org/doi/10.1145/3372782.3406251">Open Paper</a
						>
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">ToUCH</h4>
						<p class="card-text d-inline-block">
							ToUCH is a collaborative project between Texas State University, Concordia University
							and Knox College, this is an NSF funded project. We developed novel teaching materials
							for undergraduate students on how to program and use Heterogeneous Computing Systems.
							We are using a combination of Heterogeneous systems for our materials such as the
							Raspberry Pi and mobile phones based on the ARM big.LITTLE architecture and
							supercomputing systems with Nvidia cards that support CUDA programming. I was a part
							of the first team that setup the project and started development on course materials
							while at Knox.
						</p>
						<button
							class="poster-toggle"
							aria-label="Toggle ToUCH poster"
							aria-expanded={!!openSections.touch}
							onclick={() => toggle('touch')}><Icon name="spreadsheet" /></button
						>
						{#if openSections.touch}
							<div transition:slide={{ duration: 250 }}>
								<iframe class="poster" src="/Poster_RPI.pdf" title="ToUCH poster"></iframe>
							</div>
						{/if}
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Dragonfly</h4>
						<p class="card-text d-inline-block">
							Dragonfly is a High Performance Computer topology, our project was funded by an NSF
							grant. Working alongside one other student and our advisor Prof. David Bunde, we
							developed an algorithm to map tasks onto a dragonfly system. I presented our work at
							various conferences and at the 2018 Consortium of Computing Science Colleges: MidWest
							Conference we were awarded 1st place for our work.
						</p>
						<button
							class="poster-toggle"
							aria-label="Toggle Dragonfly poster"
							aria-expanded={!!openSections.dragonfly}
							onclick={() => toggle('dragonfly')}><Icon name="spreadsheet" /></button
						>
						{#if openSections.dragonfly}
							<div transition:slide={{ duration: 250 }}>
								<iframe class="poster" src="/Poster_Dragonfly.pdf" title="Dragonfly poster"
								></iframe>
							</div>
						{/if}
					</div>
				</div>
			</div>
		{/if}
	</section>

	<section class="page-section">
		<div class="section-heading d-flex justify-content-between mx-4">
			<h2>Experiences</h2>
			<button
				class="toggle-button"
				aria-label="Toggle Experiences"
				aria-expanded={!!openSections.experiences}
				onclick={() => toggle('experiences')}
				><Icon name="patch-plus" class="section-icon" /></button
			>
		</div>
		{#if openSections.experiences}
			<div class="section-content mt-2" transition:slide={{ duration: 250 }}>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Work Experiences</h4>
						<div class="card-body">
							Software Engineer Intern (Part Time) -- Incentifind, Inc <b>|</b> PHP, GraphQL,
							Laravel, React, SQLSRV, AWS, Sentry, Forge<br /><br />
							Software Engineer -- TWST Events (Acquisition of CSS) <b>|</b> Java, Groovy, Grails,
							MySQL, Postgres, Firebase, Next.js, Vue.js, React, Apache, Perl, AWS, GCP <br /><br />
							Full-Stack Developer -- StreamEngine.io <b>|</b> Python, Django, React <br />
						</div>
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Academic Experiences</h4>
						<div class="card-body">
							Graduate Teaching Assistant for Advanced Machine Learning Courses <b>|</b> Graduate
							Research Assistant <b>|</b> School of Engineering and Applied Science Ambassador
							<br /><br />
							Teaching Assistant for 4 courses in Java; Object Oriented Programming, Data Structures (Maps,
							Arrays, Linked Lists, Trees, Stacks), Algorithm Design &amp; Analysis (BFS/DFS, A*, Sorting,
							Binary Search), Programming Languages <b>|</b> Resident Assistant Feb 2018 - Jun 2019
							<b>|</b>
							Alumni Ambassador President Mar 2017 - Jun 2020 <b>|</b> Computer Science Tutor Sept
							2017 - Jun 2020 <b>|</b> Orientation Leader Aug 2017 - Sept 2017
						</div>
					</div>
				</div>
			</div>
		{/if}
	</section>

	<section class="page-section">
		<div class="section-heading d-flex justify-content-between mx-4">
			<h2>Projects</h2>
			<button
				class="toggle-button"
				aria-label="Toggle Projects"
				aria-expanded={!!openSections.projects}
				onclick={() => toggle('projects')}><Icon name="patch-plus" class="section-icon" /></button
			>
		</div>
		{#if openSections.projects}
			<div class="section-content mt-2" transition:slide={{ duration: 250 }}>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Zing</h4>
						<p class="card-text d-inline-block">
							Cross Platform iOS and Android application made using React Native and Firebase. This
							was my startup venture that provides a solution for finding events near you that are
							catered to your interests.
						</p>
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">B.L.O.B</h4>
						<p class="card-text d-inline-block">
							Android application made using Unity, team based project for CS 292. Work was divided
							into 3 sprints each a week long and our overall goal was to incorporate awareness of
							climate change into it.
						</p>
					</div>
				</div>
				<div class="card m-4">
					<div class="card-body">
						<h4 class="card-title">Scrub</h4>
						<p class="card-text d-inline-block">
							Cross Platform iOS and Android application made using React Native and Expo
							development stack. Scrub teaches you the correct way to wash your hands as suggested
							by the CDC and WHO. App is also hosted as a snack.
						</p>
					</div>
				</div>
			</div>
		{/if}
	</section>

	<section class="page-section">
		<div class="section-heading d-flex justify-content-between mx-4">
			<h2>Research CV</h2>
			<button
				class="toggle-button"
				aria-label="Toggle Research CV"
				aria-expanded={!!openSections.researchCv}
				onclick={() => toggle('researchCv')}><Icon name="patch-plus" class="section-icon" /></button
			>
		</div>
		{#if openSections.researchCv}
			<div class="section-content mt-2" transition:slide={{ duration: 250 }}>
				<div class="card m-4">
					<div class="card-body">
						<iframe class="document" src="/ArsalanBinNajeeb_ResearchResume.pdf" title="Research CV"
						></iframe>
					</div>
				</div>
			</div>
		{/if}
	</section>

	<section class="page-section mb-4">
		<div class="section-heading d-flex justify-content-between mx-4">
			<h2>Resume</h2>
			<button
				class="toggle-button"
				aria-label="Toggle Resume"
				aria-expanded={!!openSections.resume}
				onclick={() => toggle('resume')}><Icon name="patch-plus" class="section-icon" /></button
			>
		</div>
		{#if openSections.resume}
			<div class="section-content mt-2" transition:slide={{ duration: 250 }}>
				<div class="card m-4">
					<div class="card-body">
						<iframe class="document" src="/ArsalanBinNajeeb_Resume.pdf" title="Resume"></iframe>
					</div>
				</div>
			</div>
		{/if}
	</section>
</main>
