<template>
  <div>
    <a class="button is-warning" @click="open">
      <span class="icon">
        <i class="fas fa-map"></i>
      </span>
      <span>
        map
      </span>
    </a>

    <div class="modal" :class="{ 'is-active': isOpen }">
      <div class="modal-background" @click="close"></div>
      <div class="modal-content">
        <div class="map-container">
          <img src="/map.png" alt="" />
        </div>
      </div>
      <button
        class="modal-close is-large"
        aria-label="close"
        @click="close"
      ></button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    open() {
      this.isOpen = true
    },
    close() {
      this.isOpen = false
    }
  }
}
</script>

<style scoped>
.modal-content {
  height: 95vh;
  text-align: center;
}
</style>
