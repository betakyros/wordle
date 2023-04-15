<script context="module" lang="ts">
	const cache = new Map<string, Promise<DictionaryEntry>>();
</script>

<script lang="ts">
	export let word: string;
	cache.set(word);
	
	export let desc: string;
	cache.set(desc);
</script>

<div class="def">
	<h2>{word}</h2>
	<ol>
		{desc}
	</ol>
</div>

<style>
	h2 {
		display: inline-block;
		margin-right: 1rem;
		margin-bottom: 0.8rem;
	}
	ol {
		padding-left: 1.5rem;
	}
	li {
		margin-bottom: 0.5rem;
	}
	li::first-letter {
		text-transform: uppercase;
	}
	li::marker {
		color: var(--fg-secondary);
	}
</style>
