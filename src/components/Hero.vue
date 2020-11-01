<template>
  <section id="hero">
    <main class="container">
      <h1>Best pizza in the world</h1>
      <p>Stop, pizza time! Go with the flow, it's said, so check out our awesome pizza today!</p>
      <CTAButtons />
    </main>
  </section>
</template>

<script>
import CTAButtons from './CTAButtons';

export default {
  name: 'Hero',
  components: {
    CTAButtons
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
section {
  background-image: url('~@/assets/pizza-hero.png');
  background-repeat: no-repeat;
  background-size: 100%;

  @media screen and (min-width: 920px) {
    background-position: 130% -30%;
    background-size: 70%;
  }

  @media screen and (min-width: 1200px) {
    background-position: 105% 0;
    background-size: 60%;
  }
}

main {
  padding: 60vw 1.5rem;
  padding-bottom: 10rem;

  @media screen and (min-width: 920px) {
    padding: 15vw 1.5rem;
    text-align: left;
  }
}

h1 {
  margin-bottom: 1.5rem;
  font-size: 3rem;

  @media screen and (min-width: 920px) {
    max-width: 50%;
  }
}

p {
  font-size: 1.2rem;

  @media screen and (min-width: 920px) {
    max-width: 50%;
  }
}
</style>
