<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Votre animal s'est égaré ?
        </h1>

        <p class="subheading font-weight-regular">
          Suivez les étapes suivantes pour procéder à sa recherche dans les
          meilleures conditions :
        </p>
      </v-col>

      <v-col class="mb-5" cols="12">
        <StepsFinding />
      </v-col>
      <v-col class="text-center">
        <p class="subheading font-weight-regular">
          <a href="https://community.vuetifyjs.com" target="_blank">
            <v-icon>mdi-facebook</v-icon> Communauté Facebook</a
          >
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import StepsFinding from '@/components/StepsFinding.vue'

export default {
  name: 'Home',
  components: {
    StepsFinding
  }
}
</script>
