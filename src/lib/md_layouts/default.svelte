<script lang="ts">
  import "./default.css"
	export let title = 'Page Title';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<main>
	<h1 class="is-size-3">{title}</h1>
	<slot />
</main>