<template>
<!--  <v-app>-->
<!--    <v-app-bar-->
<!--      app-->
<!--      color="primary"-->
<!--      dark-->
<!--    >-->
<!--      <div style="margin-left: 100px">-->
<!--        Crpto Naughty Mammal-->
<!--      </div>-->

<!--      <v-spacer></v-spacer>-->

<!--      <v-btn-->
<!--        text-->
<!--      >-->
<!--        <div class="mr-2">Home</div>-->
<!--      </v-btn>-->
<!--      <v-btn-->
<!--          text-->
<!--      >-->
<!--        <div class="mr-2">Story</div>-->
<!--      </v-btn>-->
<!--      <v-btn-->
<!--          text-->
<!--      >-->
<!--        <div class="mr-2">Specs</div>-->
<!--      </v-btn>-->
<!--      <v-btn-->
<!--          text-->
<!--      >-->
<!--        <div class="mr-2">Community</div>-->
<!--      </v-btn>-->
<!--      <v-btn-->
<!--          text-->
<!--      >-->
<!--        <div class="mr-2">Roadmap</div>-->
<!--      </v-btn>-->
<!--      <v-btn-->
<!--          text-->
<!--      >-->
<!--        <div class="mr-2">Team</div>-->
<!--      </v-btn>-->
<!--    </v-app-bar>-->

    <v-app>
      <home></home>
    </v-app>
<!--  </v-app>-->
</template>

<script>
import Home from './views/Home.vue';

export default {
  components: { Home },
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
