<template>
  <header class="site-header">
    <nav class="container">
      <nuxt-link to="/" class="home">
        <slot name="title"></slot>
      </nuxt-link>
      <div class="nav-bar">
        <slot name="link"></slot>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style lang="scss">
.site-header {
  position: absolute;
  top: 10px;
  right: 0;
  left: 0;
  z-index: 10;
  min-height: 50px;

  color: white;

  .container {
    margin: 0 auto;
    justify-content: space-between;

    display: flex;
    max-width: 1400px;
    min-height: 50px;
    align-items: center;
    padding: 0 20px;

    a {
      font-weight: 400;
      color: white;
      letter-spacing: 0.02em;

      transition: 0.2s;
      padding: 6px;
      &.home {
        font-size: 1.25rem;
      }
      &:not(.home) {
        margin-left: 6px;
      }
      &:hover {
        color: rgba(255, 255, 255, 0.45);
      }
    }
  }
}
</style>
