<script>
	import mailbox from 'bootstrap-icons/icons/mailbox.svg?raw';
	import github from 'bootstrap-icons/icons/github.svg?raw';
	import linkedin from 'bootstrap-icons/icons/linkedin.svg?raw';
	import patchPlus from 'bootstrap-icons/icons/patch-plus.svg?raw';
	import spreadsheet from 'bootstrap-icons/icons/file-earmark-spreadsheet.svg?raw';

	let { name, class: className = '' } = $props();
	const icons = { mailbox, github, linkedin, 'patch-plus': patchPlus, spreadsheet };
</script>

<!-- SVG markup comes only from the bundled Bootstrap Icons package, never user input. -->
<!-- eslint-disable-next-line svelte/no-at-html-tags -->
<span class="site-icon {className}" aria-hidden="true">{@html icons[name]}</span>
