<script>
  import Hero from '../components/Hero.svelte';
  import Search from '../components/Search.svelte';
  import Posts from '../components/Posts.svelte';
  import postsPreview from './_posts-preview.js';

</script>

<head:svelte>
  <title>News blog</title>
</head:svelte>

<Hero />
<main class="container">
  <Search />
  <Posts {postsPreview} />
</main>