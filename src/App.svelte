<!--
	Svelte REPL only works with hash-mode routing.
	See History API and SSR examples at https://github.com/bluwy/svelte-url.
-->

<script>
  import url from './url'
</script>

<nav>
  <a href="#/">Home</a>
  <a href="#/about">About</a>
  <a href="#/404">404</a>
</nav>

{#if $url.hash === '' || $url.hash === '#/'}
  <h1>Home Sweet Home</h1>
{:else if $url.hash === '#/about'}
  <h1>About What?</h1>
{:else}
  <h1>404</h1>
{/if}
