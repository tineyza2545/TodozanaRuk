<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/272709188_537143344059102_6116193726088659182_n.jpg"
          transition="scale-transition"
          width="40"
          height="45"
        />

        <h1>Tiney</h1>
      </div>

      <v-spacer></v-spacer>

      <v-btn to="/" text> <span class="mr-2">Home</span> </v-btn
      ><v-btn to="/about" text> <span class="mr-2">about</span> </v-btn
      ><v-btn to="/todo" text>
        <span class="mr-2">todo</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
