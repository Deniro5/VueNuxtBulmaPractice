<template>
  <DefaultLayout>
    <BaseHero
      title="Contact Us"
      subtitle="Get in touch with our friendly customer service staff"
    />
    <section class="columns py-6 is-centered">
      <div class="column mw-600 ">
      <h1 class="title has-text-centered has">Get In Touch!</h1>
      <p class="subtitle has-bottom has-text-centered mt-1 is-6 ">
        Fill out the form below and we will get back to you as soon as possible!
      </p>

      <div class="section container"> 
        <label class="label">Current Progress:</label>
        <progress class="progress is-primary" :value="test" max="3">15%</progress>
      </div>

      <form class="container mt-6" @submit="handleSubmit">
        <div class="field">
          <label class="label">First Name</label>
          <div class="control">
            <input v-model = "firstName"  class="input" type="text"  />
          </div>
        </div>
        <div class="field">
          <label class="label">Last Name</label>
          <div class="control">
            <input v-model = "lastName"  class="input" type="text"  />
          </div>
        </div>
        <div class="field">
          <label class="label">Email</label>
          <div class="control">
            <input v-model = "email" class="input" type="text"  />
          </div>
        </div>
        <button class="button is-info mt-5">Submit</button>

      </form>
      </div>
    </section>
  </DefaultLayout>
</template>

<script>
import BaseHero from '../components/common/BaseHero.vue'
import DefaultLayout from '../layouts/DefaultLayout.vue'
export default {
  name: 'IndexPage',
  components: { BaseHero, DefaultLayout },
  data () {
      return {
        firstName: '',
        lastName: '',
        email: '',
      }
  },
  computed: {
    test() {
      return !!this.firstName.length + !!this.lastName.length + !! this.email.length
    }
  },
  methods: {
      handleSubmit(e) {
          e.preventDefault()
          console.log(this.firstName + ' ' + this.lastName + ' ' + this.email)
      }
  }}
</script>

<style scoped>
  .mw-600 {
    max-width: 600px !important;
  }
  </style>



</style>
