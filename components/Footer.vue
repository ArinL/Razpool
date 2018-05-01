<template>
    <footer class="site-footer">
        <div class="container">
            <div class="top">

                <nuxt-link to="/" class="home">
                    <slot name="title"></slot>
                </nuxt-link>
            </div>
            <p>
                <small>Razpool © 2018</small>
            </p>
        </div>
    </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.site-footer {
  text-align: center;
  padding: 2rem 0;
  color: rgba(14, 30, 37, 0.38);
  .container {
    max-width: 60rem;
    padding: 0 2rem;
    margin: 0 auto;
    &::before {
      content: "";
      display: block;
      width: 100%;
      height: 2px;
      background-image: linear-gradient(
        -90deg,
        rgba(14, 30, 37, 0) 0,
        #0e1e25 5%,
        #0e1e25 90%,
        rgba(14, 30, 37, 0) 100%
      );
      opacity: 0.08;
    }
    .top {
      padding: 2rem 0 1rem 0;
      .home {
        font-size: 1.25rem;
        letter-spacing: 0.02em;
        transition: 0.2s;
        color: rgba(14, 30, 37, 0.8);
        &:hover {
          color: rgba(14, 30, 37, 0.6);
        }
      }
    }
  }
}
</style>

