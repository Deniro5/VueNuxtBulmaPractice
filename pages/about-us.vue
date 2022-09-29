<template>
  <DefaultLayout>
    <BaseHero
      title="About Us"
      subtitle="Learn more about our company and what we do!"
    />
    <section class="section">
      <h1 class="title has-text-centered is-primary">Meet the Team!</h1>
      <section class="section columns">
        <div class="column mx-1">
          <EmployeeCard
            name="Joe Smith"
            position="CEO"
            comment="Hi My name is Joe and im the CEO"
            imgsrc="https://t3.ftcdn.net/jpg/02/99/04/20/240_F_299042079_vGBD7wIlSeNl7vOevWHiL93G4koMM967.jpg"
          />
        </div>
        <div class="column mx-1">
          <EmployeeCard
            name="Joe Smith"
            position="CEO"
            comment="Hi My name is Joe and im the CEO"
            imgsrc="https://t3.ftcdn.net/jpg/02/99/04/20/240_F_299042079_vGBD7wIlSeNl7vOevWHiL93G4koMM967.jpg"
          />
        </div>
        <div class="column mx-1">
          <EmployeeCard
            name="Joe Smith"
            position="CEO"
            comment="Hi My name is Joe and im the CEO"
            imgsrc="https://t3.ftcdn.net/jpg/02/99/04/20/240_F_299042079_vGBD7wIlSeNl7vOevWHiL93G4koMM967.jpg"
          />
        </div>
      </section>
    </section>
  </DefaultLayout>
</template>

<script>
import BaseHero from '../components/common/BaseHero.vue'
import DefaultLayout from '../layouts/DefaultLayout.vue'
import EmployeeCard from '../components/about-us/EmployeeCard.vue'
export default {
  name: 'IndexPage',
  components: { BaseHero, DefaultLayout, EmployeeCard },
}
</script>
