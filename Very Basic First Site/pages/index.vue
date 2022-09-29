<template>
  <DefaultLayout>
    <BaseHero
      title="Welcome To My Website"
      subtitle="We hope you enjoy your stay"
    />
    <section class="section">
      <h1 class="title">Home</h1>
      <h2 class="subtitle">
        The purpose of this website is to test out Bulma and Nuxt together.
        Click <span class="modalTrigger" @click="handleClick">here</span> for
        more info.
      </h2>
    </section>
    <div v-if="isModalOpen" class="modal is-active">
      <div class="modal-background"></div>
      <div class="modal-content has-background-white p-6">
        <div class="content">
          <h1 class="title">There is no info here yet</h1>
          <h2 class="subtitle mt-6 is-5">
            Please come back in a few weeks for an update
          </h2>
        </div>
      </div>
      <button class="modal-close is-large" @click="handleCloseModal"></button>
    </div>
  </DefaultLayout>
</template>

<script>
import DefaultLayout from '../layouts/DefaultLayout.vue'
import BaseHero from '../components/common/BaseHero.vue'
export default {
  name: 'IndexPage',
  components: { DefaultLayout, BaseHero },
  data() {
    return { isModalOpen: false }
  },
  methods: {
    handleClick() {
      this.isModalOpen = true
    },
    handleCloseModal() {
      this.isModalOpen = false
    },
  },
}
</script>

<style>
@import 'https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css';
.modalTrigger {
  cursor: pointer;
  color: blue;
  text-decoration: underline;
}
</style>
