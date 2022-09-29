<template>
  <div>
    <NavBar />
    <slot />
    <AppFooter />
  </div>
</template>

<script>
import NavBar from '../components/common/NavBar.vue'
import AppFooter from '../components/common/AppFooter.vue'
export default {
  name: 'DefaultLayout',
  components: { NavBar, AppFooter },
}
</script>
