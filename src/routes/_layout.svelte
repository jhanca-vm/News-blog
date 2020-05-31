<script>
  import Header from '../components/Header.svelte';
  import Hero from '../components/Hero.svelte';
  import Footer from '../components/Footer.svelte';

  export let segment;
</script>

<Header {segment}/>
<Hero />
<main class="container">
  <slot></slot>
</main>
<Footer />