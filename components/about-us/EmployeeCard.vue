<template>
  <div class="card">
    <div class="card-image">
      <figure class="image is-4by3">
        <img :src="imgsrc" alt="Placeholder image" />
      </figure>
    </div>
    <div class="card-content">
      <div class="media">
        <div class="media-left">
          <figure class="image">
            <img
              class="diameter-48 is-rounded"
              :src="imgsrc"
              alt="Placeholder image"
            />
          </figure>
        </div>
        <div class="media-content">
          <p class="title is-4">{{ name }}</p>
          <p class="subtitle is-size-6">{{ position }}</p>
        </div>
      </div>

      <div class="content">
        {{ comment }}
        <a href="#"> #responsive </a>
        <div class="mt-2">
          <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: { type: String, required: true },
    position: { type: String, required: true },
    comment: { type: String, required: true },
    imgsrc: { type: String, required: true },
  },
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>

<style scoped>
.card-image {
  max-width: 500px;
  max-height: 500px;
  border-radius: 3px;
}

.diameter-48 {
  height: 48px;
  width: 48px;
  border: 1px solid black;
}
</style>
