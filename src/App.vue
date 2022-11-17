<template>
  <v-app>
    <v-app-bar
      app
      hide-on-scroll
      color="#8F00FF"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="img-logo"
          contain
          src="https://thumbs.dreamstime.com/b/núcleo-y-electrones-de-la-estructura-del-átomo-icono-tomo-ejemplo-vector-aislado-en-fondo-transparente-146177607.jpg"
          transition="scale-transition"
          width="50"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href=""
        target="_blank"
        text
      >
        <span class="mr-2">kirchhoff</span>
        <v-icon>{{ icons.mdiAtomVariant }}</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main style="width: 100%; padding-top:0px">
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import { mdiAccount } from '@mdi/js'
import { mdiAtomVariant } from '@mdi/js';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
     icons: { mdiAccount, mdiAtomVariant }
  }),
};
</script>
<style>
  .main-main {
    width: 100%;
  }
  .img-logo {
    border-radius: 100%;    
  }
</style>
