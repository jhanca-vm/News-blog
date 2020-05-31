<script context="module">
	export async function preload({ params, query }) {
		const res = await this.fetch(`${params.slug}.json`);
		const data = await res.json();
		if (res.status === 200) {
			return { post: data };
		} else {
			this.error(res.status, data.message);
		}
	}
</script>

<script>
	import postsPreview from './_posts';

	export let post;

	let others = postsPreview.slice(2, 5);
</script>

<style>
	.post-pic {
		width: 100%;
		height: 400px;
		background-image: url('https://picsum.photos/1000/400');
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
	}
</style>

<svelte:head>
	<title>{post.title}</title>
</svelte:head>

<section>
	<div class="row">
		<div class="col s12">
			<h2>{post.title}</h2>
		</div>
	</div>
</section>
<section>
	<div class="row">
		<div class="col m8">
			<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint voluptate autem id, hic quia dolor et eveniet quae nam laudantium assumenda, beatae aliquid aperiam temporibus omnis! Laboriosam provident nesciunt numquam!
			Exercitationem eaque reiciendis temporibus porro ea officiis? Voluptas ipsum, sit tenetur dolor accusantium aliquam minus, illum alias, nemo qui laborum a eum. Magni nemo nam obcaecati qui, iure maxime aut?
			Repellat blanditiis ratione iusto, rerum incidunt placeat accusamus, aspernatur sit unde tempore eum nobis porro laudantium, at labore. Beatae deleniti laboriosam repudiandae quidem magnam ipsum amet expedita voluptatum officia numquam?
			Porro accusamus dolor esse nihil a maxime non molestias eius tempora, quos modi corrupti, quasi voluptatibus excepturi. Quia commodi nostrum at quisquam necessitatibus deserunt illum excepturi sunt minus. Voluptas, architecto.
			Consequuntur, quas repellendus voluptas ipsum voluptates officia? Culpa nemo voluptas quaerat error alias perspiciatis suscipit! Enim esse labore velit aperiam obcaecati voluptatem a! Necessitatibus, dolores! Dolores exercitationem distinctio vel autem?
			Beatae dolores esse nobis ipsa architecto facere sed? Totam necessitatibus error cum. Veniam laborum aspernatur rerum tempore cum aut ut error ducimus maiores, inventore facilis voluptatem doloribus saepe voluptate voluptatum!
			Minus doloribus velit quasi, sunt facilis at perferendis soluta saepe natus voluptatum in eaque non accusamus nihil magnam! Soluta sequi rerum fugiat repellat deserunt iste explicabo magni dolore consequuntur repudiandae.
			Ex reiciendis voluptates facilis ut incidunt omnis delectus ea placeat accusantium minima voluptate beatae sapiente non dignissimos facere, porro adipisci dicta impedit laudantium officiis tenetur voluptas! Officia dolorum consequuntur iusto.</p>
		</div>
		<div class="col m4">
			<div class="card blue-grey darken-1">
        <div class="card-content white-text">
          <span class="card-title">Título</span>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Non maxime voluptas ab dolores id quia minima similique, porro adipisci iste assumenda sequi velit iusto minus. Dolorum, architecto commodi! Quae, odio.</p>
        </div>
			</div>
		</div>
	</div>
</section>
<section class="section">
	<div class="row">
		<div class="post-pic z-depth-2"></div>
	</div>
</section>
<section>
  <div class="row">
    {#each others as post}
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