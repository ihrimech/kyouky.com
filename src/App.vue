<template>
  <v-app>
    <v-app-bar app color="cyan" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Kyouky Logo"
          class="shrink mr-2"
          contain
          src="./assets/black-cat.svg"
          transition="scale-transition"
          width="40"
        />

        <router-link to="/">
          <h1
            alt="kyouky Name"
            class="shrink mt-1 hidden-sm-and-down"
            contain
            min-width="100"
          >
            KYOUKY
          </h1>
        </router-link>
      </div>

      <v-spacer></v-spacer>

      <router-link to="/about">
        <span class="mr-2">A propos</span>
        <v-icon>mdi-information</v-icon>
      </router-link>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App'
}
</script>
