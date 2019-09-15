<template>
  <v-app>
    <v-content>
      <main>
         <router-view/>
      </main>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>

<style>
  body {
    padding: 0;
  }
  @font-face {
    font-family: Montserrat;
    src: url(./assets/fonts/Montserrat-Regular.ttf);
  }
</style>

