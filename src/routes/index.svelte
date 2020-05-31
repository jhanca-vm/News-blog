<script>
  import Search from '../components/Search.svelte';
  import Posts from '../components/Posts.svelte';
  import postsPreview from './_posts.js';

</script>

<head:svelte>
  <title>News blog</title>
</head:svelte>

<Search />
<Posts {postsPreview} />