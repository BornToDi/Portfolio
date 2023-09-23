<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-black">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
        <q-toolbar-title> ZIHADUL PORTFOLIO </q-toolbar-title>
        <!-- <div>Quasar v{{ $q.version }}</div> -->
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <div>
        <q-img
          class="absolute-top"
          src="~assets/cover.png"
          style="height: 200px"
        >
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="100px" class="q-mb-sm">
              <img src="~assets/mypic.png" />
            </q-avatar>
            <div class="text-weight-bold">MD ZIHADUL ISLAM</div>
            <div>Web Developer</div>
          </div>
        </q-img>
      </div>
      <div>
        <q-scroll-area
          style="
            height: calc(100% - 150px);
            margin-top: 200px;
            border-right: 1px solid #ddd;
          "
        ></q-scroll-area>
        <q-list>
          <q-item-label header>My Essential Links </q-item-label>

          <EssentialLink
            v-for="link in essentialLinks"
            :key="link.title"
            v-bind="link"
          />
        </q-list>
      </div>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- Footer -->
    <q-footer class="bg-black absolute-bottom">
      <div class="row justify-center items-center py-5 text-lg">
        2023 © Zihadul™ All rights reserved.
      </div>
    </q-footer>
  </q-layout>
</template>
<script>
import EssentialLink from "components/EssentialLink.vue";

const linksList = [
  {
    title: "Educations & CV",
    caption:
      "American International University Bangladesh --    BSC in CSE (2018-2023)",
    icon: "school",
    link: "https://drive.google.com/file/d/1XmNeMYINNBvpHPUxb78hYlPlVlcqxiPS/view?usp=drive_link",
  },
  {
    title: "Github",
    caption: "github.com/BornToDi",
    icon: "code",
    link: "https://github.com/BornToDi",
  },
  // {
  //   title: "Discord Chat Channel",
  //   caption: "chat.quasar.dev",
  //   icon: "chat",
  //   link: "https://chat.quasar.dev",
  // },
  {
    title: "Facebook",
    caption: "facebook/MD Zihadul Islam",
    icon: "facebook",
    link: "https://www.facebook.com/the.leader.will.come.one.day?mibextid=ZbWKwL",
  },

  {
    title: "Linkedin",
    caption: "Linkedin/Zihadul",
    icon: "task_alt",
    link: "",
  },
  // {
  //   title: "Quasar Awesome",
  //   caption: "Community Quasar projects",
  //   icon: "favorite",
  //   link: "https://awesome.quasar.dev",
  // },
];

import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
