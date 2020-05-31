<script>
  export let postsPreview;
</script>

<section>
  <div class="row">
    {#each postsPreview as post}
      <article class="col s12 m6 l4">
        <div class="card">
          <div class="card-image waves-effect waves-block waves-light">
            <img class="activator" src={post.image} alt={post.title}>
          </div>
          <div class="card-content">
            <span class="card-title activator grey-text text-darken-4">{post.title}<i class="material-icons right">more_vert</i></span>
          </div>
          <div class="card-reveal">
            <span class="card-title grey-text text-darken-4">{post.title}<i class="material-icons right">close</i></span>
            <p>{post.description}</p>
            <a class="waves-effect waves-tail btn-flat teal lighten-5 right" href={post.slug}>Ir</a>
          </div>
        </div>
      </article>
    {/each}
  </div>
</section>