<template>
  <div>
    <!-- Estoy en bulma -->
    <main class="container">
      <article class="row">
        <section class="img show">
          <img v-bind:src="getImgUrl()">
        </section>
        <section class="others">
          <div class="guide__travel show" >
            <h4>Guía</h4>
            <img src="../assets/compass.svg" alt>
            <span></span>
            <p>{{ sites[j].country }}</p>
          </div>
          <h1>{{ sites[j].state }}</h1>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quis rerum harum ut saepe dicta.</p>
          <div class="area">
            <p>
              Area:
              <span>
                {{ sites[j].area }} KM
                <sup>2</sup>
              </span>
            </p>
            <p>
              Logitud máxima:
              <span>
                {{ sites[j].maxLength }} KM
                <sup>2</sup>
              </span>
            </p>
          </div>

          <div class="card__bottom">
            <img v-bind:src="getImgUrl()" class="img-hide" alt>
            <div class="card arrow">
              <h3>
                Encontrar
                <br>hoteles
              </h3>
              <p>
                <i></i>
                <i></i>
              </p>
            </div>
            <div class="card">
              <h3>
                Encontrar
                <br>vuelo
              </h3>
              <img src="../assets/grecia.svg" alt>
            </div>
          </div>
        </section>

        <section class="eje__y">
          <div class="count">
            <span>{{ count }}</span>
            <span></span>
            <span>{{ countAll }}</span>
          </div>
          <div class="arrows">
            <div @click="j < end ? j++ : ''" :class="['arrow', {'none': j >= end}]">
              <!-- Siguiente -->
              <p>
                <i></i>
                <i></i>
              </p>
            </div>
            <div @click="j <= end ? j-- : ''" :class="['arrow', {'none': j == 0}]">
              <!-- Anterior -->
              <p>
                <i></i>
                <i></i>
              </p>
            </div>
          </div>
        </section>
      </article>
      <footer>
        <a href="#">Inspiration</a>
        <a href="#">Github</a>
      </footer>
    </main>
  </div>
</template>

<style lang="scss" scoped>
@import "../scss/responsive";
@import "../scss/main";
@import "../scss/keyframes";
</style>
<script>
export default {
  props: ["sites"],
  data() {
    return {
      j: 0,
      end: this.sites.length -1,
    };
  },
  methods: {
       onImgLoad () {
      this.isLoaded = true
    },
    getImgUrl() {
      var images = require.context("../assets/", false);
      return images("./" + this.sites[this.j].nameImg);
    },
    onWindowLoad(){
        console.log('Cargado')
    }
  },
  computed: {
    countAll() {
      return this.sites.length >= 10
        ? this.sites.length
        : "0" + this.sites.length;
    },
    count() {
      return this.sites.length >= 10 ? this.j + 1 : this.j + 1;
    }
  },
  mounted() {
    //    this.nextPrev()
    console.log(this.j);
    
  },
  create() {
        document.querySelector('img').addEventListener("load", this.onWindowLoad);
    },
};
</script>