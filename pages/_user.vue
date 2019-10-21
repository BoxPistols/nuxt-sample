<template name="component-name">
  <div>
    <div>
      <!-- {{ $route.params.user }} -->
      <img :src="avatar_url" width="100">
      <span>{{ name }}</span>
    </div>
    <a :href="html_url">
      {{ html_url }}
    </a>
  </div>
</template>
<script>
export default {
	name: 'user',
	async asyncData({ app, params }) {
		if (process.server) {
			console.log('server');
		}
		if (process.client) {
			console.log('client');
		}
		const data = await app.$axios.$get(`https://api.github.com/users/${params.user}`);
		return data;
	},
};
</script>

<style>
body {
	text-align: center;
}
a {
	color: tomato;
}
</style>
