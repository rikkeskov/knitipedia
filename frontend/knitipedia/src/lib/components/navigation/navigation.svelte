<script>
	export let links = [
		{ name: 'Home', href: '/' },
		{ name: 'Patterns', href: '/patterns' },
		{ name: 'Yarns', href: '/yarns' },
		{ name: 'About', href: '/about' }
	];
</script>

<nav class="border-b border-gray-200 bg-gray-50 p-4">
	<ul class="m-0 flex list-none gap-6 p-0">
		{#each links as link}
			<li>
				<a
					href={link.href}
					class="font-medium text-gray-800 no-underline transition-colors duration-200 hover:text-blue-600"
				>
					{link.name}
				</a>
			</li>
		{/each}
	</ul>
</nav>
