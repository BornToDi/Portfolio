<template>
  <div class="q-pa-md">
    <q-carousel
      :ratio="4 / 3"
      animated
      v-model="slide"
      swipeable
      infinite
      arrows
      :autoplay="autoplay"
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = false"
      @mouseleave="autoplay = true"
    >
      <q-carousel-slide name="first" img-src="~assets/welcome.jpg">
        <div class="absolute-center custom-caption">
          <div class="text-4xl">Hello! This is MD Zihadul Islam</div>
          <div class="text-lg">
            Frontend Developer | Cross Platform Software
          </div>
          <!-- My CV -->
          <transition
            appear
            enter-active-class="animated fadeIn"
            leave-active-class="animated fadeOut"
          >
            <q-btn
              class="py-3 my-4 bg-gray-700 rounded-lg"
              icon="collections_bookmark"
              label="My CV"
              href="https://drive.google.com/file/d/1XmNeMYINNBvpHPUxb78hYlPlVlcqxiPS/view?usp=drive_link"
            />
          </transition>
          <!-- My Professional Achievements -->
          <transition
            appear
            enter-active-class="animated fadeIn"
            leave-active-class="animated fadeOut"
          >
            <q-btn
              class="py-3 my-4 bg-gray-700 rounded-lg"
              icon="workspace_premium"
              label="My Professional Achievements"
              href=""
            />
          </transition>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="second" img-src="~assets/img2.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h3">Vue JS</div>
          <div class="text-subtitle1">I working with this framework.</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="third" img-src="~assets/background.png">
        <div class="absolute-bottom custom-caption">
          <div class="text-h3">Quasar JS</div>
          <div class="text-subtitle1">I working with this framework</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="fourth" img-src="~assets/react.png">
        <div class="absolute-bottom custom-caption">
          <div class="text-h3">React JS</div>
          <div class="text-subtitle1">I working with this framework</div>
        </div>
      </q-carousel-slide>
    </q-carousel>
  </div>
  <div class="text-h4 row justify-center items-center">About Me</div>

  <!-- Break -->

  <!-- <div class="flex-break q-py-md"></div> -->
  <div class="q-pa-md text-lg">
    <div class="items-left text-cyan-500 py-2">
      Frontend Developer (Software) | Vue.js | Quasar js | Figma | Javascript |
      Git.
    </div>

    I completed an Internship on Vue js & Quasar at Iching Lab
    <span class="text-cyan-500">( https://ichinglab.com/#/ )</span> . There was
    spent great time ever , I was learned many programming to be a Frontend
    developer like - Javascript , Vue , Quasar , VueX , Rest APIs , Git, Time
    managements , Company behavior , Responsibility and many more .
    <div>
      Now I'm responsible as a Frontend Developer . Now working at Iching Lab in
      project base job.
    </div>
  </div>

  <!-- My Experiences -->
  <div class="text-h4 row justify-center items-center pt-10">
    My Experiences
  </div>

  <!-- Break -->

  <div class="flex-break q-py-md"></div>

  <!-- My Experiences -->

  <div class="text-h5 row justify-center items-center pb-10">
    <div class="flex flex-center">
      <q-btn href="https://vuejs.org/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img4.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://quasar.dev/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img5.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://www.w3schools.com/js/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img6.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://www.google.com/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img7.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>

      <q-btn href="https://github.com/BornToDi">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img10.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
    </div>
  </div>

  <!-- About Me Popup -->

  <div class="q-pa-md q-gutter-sm fixed-bottom-right">
    <q-btn
      icon="favorite"
      round
      class="q-ma-md"
      color="black"
      @click="alert = true"
    />
    <q-dialog v-model="alert">
      <q-card>
        <q-card-section>
          <div class="text-h6">About me</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          Frontend Developer | Vue.js | Quasar js | React js | Javascript | Git
          <br />
          Internship Completed at Iching Lab(Software Company) <br />
          Working as Project based job .
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      slide: ref("first"),
      autoplay: ref(true),
      alert: ref(false),
      prompt: false,
      submit: " ",
      cancel: "",
    };
  },
};
</script>

<style lang="sass" scoped>
.custom-caption
  text-align: center
  padding: 12px
  color: white
  background-color: rgba(0, 0, 0, .3) ,

.my-emoji
  vertical-align: middle
  height: 2em
  width: 2em
</style>
<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>
