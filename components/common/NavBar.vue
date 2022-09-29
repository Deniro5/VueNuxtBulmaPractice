<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="https://bulma.io">
        <img
          src="https://placeholder.com/wp-content/uploads/2018/10/placeholder.com-logo1.png"
          width="112"
          height="28"
        />
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start pl-6">
        <NuxtLink to="/" class="navbar-item"> Home </NuxtLink>
        <NuxtLink to="/about-us" class="navbar-item"> About </NuxtLink>
        <NuxtLink to="/contact-us" class="navbar-item"> Contact Us </NuxtLink>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
