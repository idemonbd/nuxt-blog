<template>
	<div class="main">
		<section id="LatestPosts" class="container">
			<div class="card">
				<div class="card-header">
					<h4 class="text-center">Latest Blogs</h4>
				</div>
				<div class="card-body">

					<div v-if="loading" class="loader text-center m-5 p-5">
            <div class="spinner-grow" role="status"></div>
          </div>

					<ul class="list-group">
						<li
							v-for="(post, index) in posts"
							:key="index"
							class="d-flex list-group-item"
						>
							<img
								class="mx-2 rounded"
								:src="post.image"
								alt=""
							/>
							<div class="p-3">
								<nuxt-link :to="`blog/${post.slug}`">{{ post.title }}</nuxt-link>
								<p>{{ post.description }}</p>
							</div>
						</li>
					</ul>
				</div>
			</div>
		</section>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				posts: [],
				loading: true,
			};
		},
		async fetch() {
			this.posts = await fetch("https://api.nuxtjs.dev/mountains")
      .then((res) => res.json())
      this.loading = false
      },
	};
</script>

<style lang="css">
	section {
		padding: 20px;
    transition: 0.5s;
	}

	ul li img {
		max-width: 200px;
	}
</style>
