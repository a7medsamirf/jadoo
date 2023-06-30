<template>
  <section class="hero" id="hero">
    <v-container>
    <div class="hero-wrap">
      <div class="inner d-flex align-center justify-center">
        <v-container>
          <v-row align="center" justify="center">
            <v-col cols="12" md="5" class="px-0">
              <div class="box">

          <div class="title2">
            <h3 class="ma-5 default--text">
              {{ $t('HeroSection.subtitle') }}
            </h3>
              <h1 class="ma-5 text-color-default hero-title ">
                {{ $t('HeroSection.title') }}</h1>
          </div>

          <div class="role">
              <div class="block"></div>
              <p class="use-text-subtitle ma-5 hero-subtitle">
                {{ $t('HeroSection.description') }}

              </p>
          </div>

          <div class="button-box ma-5">
          <button href="#" title="تواصل معنا" class="btn outline">{{ $t('common.Find-more') }}</button>
          <button  href="#" title="تواصل معنا" class="btn default ma-5 pa-5"> {{ $t('common.discuss') }}</button>
        </div>
        </div>
            </v-col>
            <v-col cols="12" md="7" class="px-0 mt-16">
              <div class="img-box hidden-sm-and-down">
                <v-img
                  class="hero-img"
                  alt="hero"
                  :lazy-src="require('static/images/hero/Traveller1.png')"
                  :src="require('static/images/hero/Traveller1.png')"
                >
                </v-img>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </div>
    </v-container>
  </section>

</template>

<script>
export default {
  name: "Hero"
}
</script>


<style scoped lang="scss">
#hero{
  background-image: url(#{$HeroBgPath}/Decore.png) !important;
  background-size: contain !important;
  background-position: 100% 0%;
  .hero-wrap{
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  align-items: center;
  position: relative;
  display: block;
  height: 100vh;
  .hero-title {
    position: relative;
    text-transform: capitalize;
    font-size: 5.375rem !important;
    font-weight: 900;
    z-index: 5;
    font-family: $title-font-family;
    @include breakpoints-down(md) {
      font-size: 2.625rem !important;
    }
    &::after{
        content:'';
        background-image: url(#{$HerotitlePath}/Decore2.png) !important;
        position: absolute;
        left: 285px;
        width: 320px;
        height: 20px;
        top: 90px;
        z-index: -1;
    }
  }
  .inner {
    height: 100%;
  }

}

}

.hero-img{
  &::after{
    content:'';
    background-image: url(#{$HeroPlanePath}/plane.png) !important;
    position: absolute;
    left: 200px;
    width: 150px;
    height: 140px;
    animation: myAnim 4s ease-out 0s infinite alternate forwards;
  }
  &::before{
    content:'';
    background-image: url(#{$HeroPlanePath}/plane.png) !important;
    position: absolute;
    right: 0px;
    width: 150px;
    height: 140px;
    animation: myAnim 2s ease-out 0s infinite alternate forwards;
  }
}
@keyframes myAnim {
  0% {
    transform: translateY(0);
  }

  100% {
    transform: translateY(-20px);
  }
}

</style>
