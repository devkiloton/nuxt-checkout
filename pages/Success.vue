<template>
  <div class="py-5 text-center">
    <h2>Success</h2>
    <p class="lead">Your purchase has been completed!</p>
  </div>
</template>

<script>
export default {
  name: 'Success',
  async mounted() {
    await this.$axios.post('orders/confirm', {
      source: this.$route.query.source,
    })
  },
}
</script>

<style lang="scss" scoped></style>
