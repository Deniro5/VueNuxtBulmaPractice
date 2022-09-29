<template>
  <div>
    <section class="hero has-background-info-dark p-6">
      <div class="hero-body">
        <p class="title has-text-white">{{ title }}</p>
        <p class="subtitle has-text-white">{{ subtitle }}</p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  props: {
    title: { type: String, default: '' },
    subtitle: { type: String, default: '' },
  },
}
</script>

<style scoped></style>
