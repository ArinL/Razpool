<template>
  <main>
    <section class="top">
      <div class="content">
        <div class="text">
          <h1>Pool and Spa</h1>
          <h2>Service and Maintenance</h2>
          <h3>Call:
            <b>818-280-7887</b>
          </h3>
        </div>
      </div>
      <svg viewbox="0 0 100 25">
        <path fill="#f1f5f9" d="M0 30 V12 Q30 17 55 12 T100 11 V30z" />
      </svg>
    </section>
    <section>
      <div class="content"></div>
    </section>
  </main>
</template>

<script>
// import AppLogo from '~/components/AppLogo.vue'

// export default {
//   components: {
//     AppLogo
//   }
// }
</script>

<style lang="scss" scoped>
main {
  section {
    min-height: 50vh;
  }
  .content {
    max-width: 1400px;
    padding: 0 20px;
    margin: 0 auto;
  }
  .top {
    position: relative;
    min-height: 70vh;
    position: relative;
    background: url("~/assets/hero.jpg");
    background-size: cover;
    background-position: center 40%;
    .content {
      min-height: 70vh;
      display: flex;
      align-items: center;
      &::after {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        opacity: 0.9;

        // background: radial-gradient(farthest-side at 60% 55%, #3b78e7, #77a1ee);
        background: radial-gradient(
          farthest-side at 65% 50%,
          rgba(59, 120, 231, 0.6),
          #3b78e7
        );
      }
      .text {
        line-height: 1.4;
        color: rgba(255, 255, 255, 0.86);
        z-index: 10;
        margin-top: -8%;
        margin-left: 3%;
        h1 {
          font-size: 3.5rem;
          font-weight: 400;
        }
        h2 {
          font-size: 1.5rem;
          font-weight: 400;
        }
        h3 {
          margin-top: 1rem;
          font-size: 1.5rem;
          font-weight: 300;
        }
      }
    }
    svg {
      position: absolute;
      bottom: -90px;
      right: 0;
      left: 0;
      z-index: 10;
    }
    @media (max-width: 900px) {
      background-position: 70% 40%;
      svg {
        bottom: -30px;
      }
    }
  }
}
</style>

