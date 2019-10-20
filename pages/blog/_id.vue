<template name="component-name">
  <div class="container pd-4">
    <h2>Blog Detail</h2>
    <p>{{ $route.params.id }} ページ</p>
</div>
</template>

<script>
export default {
  validate({ params }) {
    return /^\d+$/.test(params.id)
  }
}
</script>
