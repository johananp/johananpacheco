<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="https://s.gravatar.com/avatar/818865ad86503b963d619109d7dde432?s=180" width="360" height="360" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			My thoughts
		</p>

		<p class="author__links">
			<a href="//twitter.com/PachecoJohanan">Follow on Twitter</a>
			<a href="//github.com/johananp">GitHub</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 180px;
		height: 180px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
