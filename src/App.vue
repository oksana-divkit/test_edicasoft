<template>
  <main id="app">
    <div class="hero">
      <div class="container hero__container">
        <section class="hero__content">
          <p class="hero__legend">GET STARTED WITHIN 2 MINUTES</p>
          <h1 class="hero__title">Learn How To Bake In <nobr>5 Easy</nobr> Steps</h1>

          <p>No doubt, you need more one pot dinners in your life like this easy Bosnian-style chicken and rice. This recipe is made all over the world with countless variations on the theme.</p>
        </section>

        <div class="hero__form">
          <form-download />
        </div>
      </div>

      <picture class="hero__photo" aria-role="presentation">
        <source media="(max-width: 700px)" srcset="../public/images/hero-bg-s.jpg">
        <source media="(max-width: 1200px)" srcset="../public/images/hero-bg-m.jpg">
        <img src="../public/images/hero-bg.jpg" />
      </picture>
    </div>

    <article class="article container">
      <picture class="article__photo">
        <source media="(max-width: 550px)" srcset="../public/images/image-1s.jpg">
        <source media="(max-width: 850px)" srcset="../public/images/image-1m.jpg">
        <img src="../public/images/image-1.jpg" alt="White cake" />
      </picture>

      <div class="article__content">
        <h2 class="article__title">Do you know how to level a cake?</h2>

        <p>After years of cake successes and flops, I’m confident in this homemade vanilla cake. During my recipe testing, I combined my white cake recipe and naked cake recipe. These are two reader favorites and I knew they’d be the best starting point. </p>
      </div>
      
    </article>

    <article class="article article--right container">
      <picture class="article__photo">
        <source media="(max-width: 550px)" srcset="../public/images/image-2s.jpg">
        <source media="(max-width: 850px)" srcset="../public/images/image-2m.jpg">
        <img src="../public/images/image-2.jpg" alt="Vanilla Cake" />
      </picture>

      <div class="article__content">
        <h2 class="article__title">Vanilla Cake Success Tips</h2>

        <p>I always eyeball the amount of frosting between cake layers, but I measured when I decorated the pictured cake. The vanilla buttercream recipe below yields about 6 cups of frosting. I recommend you use about 1.5 heaping cups of buttercream between each cake layer and reserve the last 3 cups for outside the cake.</p>
      </div>
      
    </article>

  </main>
</template>

<script>
//import formDownLoad from './components/form-download';
var formDownLoad = require('./components/form-download').default;

export default {
  name: 'app',
  components: { 'form-download': formDownLoad },
  data: function () {
    return {
      count: 0
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Open+Sans:wght@400;700;300&display=swap');

@import 'styles/_var.scss';


* {
  box-sizing: border-box;
}

body,
html {
  padding: 0;
  margin: 0;
}

body {
  font: 16px/1.75 'Open Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $clr-text;
}

img {
  max-width: 100%;
  height: auto;
}

.container {
  max-width: 1130px;
  padding: 0 15px;
  margin: 0 auto;

  @media (min-width: 400px) {
    padding: 0 30px;
  }
}

.hero {
  position: relative;
  margin: 0 0 40px;
  background: $clr-l-primary;

  @media (min-width: 1200px) {
    margin-bottom: 70px;
  }

  &__container {
    position: relative;
    max-width: 1318px;
    padding-top: 36px;
    padding-bottom: 51px;
    z-index: 10;

    @media (min-width: 700px) {
      display: flex;
      align-items: center;
      align-content: center;
      min-height: 770px;
      padding-top: 60px;
      padding-bottom: 58px;
    }

    @media (max-width: 1380px) and (max-height: 800px) {
      // padding-top: 20px;
      // padding-bottom: 20px;
      min-height: 0;
    }
  }

  &__photo {
    position: absolute;
    top: 0;
    left: 84%;
    right: 0;
    bottom: 0;

    @media (min-width: 700px) {
      left: 73%;
    }

    @media (min-width: 1200px) {
      left: 50%;
    }

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center right;
    }
  }

  &__content {
    flex: 0 0 50%;
    min-width: 0;
    padding: 15px 15% 0 0;
    margin: 0 0 38px;

    @media (min-width: 700px) {
      padding-right: 8%;
      margin-bottom: 0;
    }

    @media (min-width: 1200px) {
      flex-basis: 33.33%;
      padding: 40px 11% 0 0;
    }
  }

  &__legend {
    margin: 0 0 .6em;
    font-weight: bold;
    font-size: 14px;
    line-height: 1.43;
    letter-spacing: 1.08333px;
    text-transform: uppercase;
    color: #999999;
  }

  &__title {
    margin: 0 0 .8em;
    font-size: 30px;
    line-height: 1.27;
    letter-spacing: -1.27273px;
    color: #000000;

    @media (min-width: 700px) {
      margin-bottom: .95em;
    }
  }

  &__form {
    flex: 0 0 50%;
    min-width: 0;

    @media (min-width: 700px) {
      padding: 0 0 0 10px;
    }

    @media (min-width: 1200px) {
      flex-basis: 33.33%;
      padding-right: 10px;
    }
  }
}

.article {
  margin-bottom: 38px;

  @media (min-width: 550px) {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 22px;
  }

  @media (min-width: 850px) {
    margin-bottom: 50px;
  }

  &--right {

    @media (min-width: 850px) {
      flex-direction: row-reverse;
    }
  }

  &__photo {
    display: block;
    margin: 0 0 13px;

    @media (min-width: 550px) {
      flex: 0 0 49%;
      margin: 0 49px 0 0;
    }

    @media (min-width: 850px) {
      flex-basis: 59%;
      margin-right: 0;
    }

    img {
      width: 100%;
    }
  }

  &__content {
    flex: 1;

    @media (min-width: 850px) {
      flex: 0 0 34.3%;
      padding: 20px 10px 0 0;
    }
  }

  &__title {
    margin: 0 0 .7em;
    font-weight: bold;
    font-size: 22px;
    line-height: 1.55;
    letter-spacing: -0.5px;
    color: #000000;

    @media (min-width: 550px) {
      margin-bottom: 1.3em;
    }
  }
}

</style>
