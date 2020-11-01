<template>
  <v-stepper v-model="e6" vertical>
    <v-stepper-step :complete="e6 > 1" step="1">
      <p>
        Déclarez votre animal perdu sur
        <a href="https://www.i-cad.fr/"> https://www.i-cad.fr/ </a>
      </p>
      <small
        >Vous devez pour cela être muni de son numéro d'identification</small
      >
    </v-stepper-step>

    <v-stepper-content step="1">
      <StepIcad />
      <v-btn color="primary" @click="e6 = 2">
        Etape suivante
      </v-btn>
    </v-stepper-content>

    <v-stepper-step :complete="e6 > 2" step="2">
      Prévenir les voisins directs
      <small
        >si possible dans un rayon de 200m par journée d'absence. Ils sont
        susceptible de voir votre animal en premier.</small
      >
    </v-stepper-step>

    <v-stepper-content step="2">
      <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
      <v-btn color="primary" @click="e6 = 3">
        Etape suivante
      </v-btn>
      <v-btn text @click="e6 = 1">
        Etape précédente
      </v-btn>
    </v-stepper-content>

    <v-stepper-step :complete="e6 > 3" step="3">
      Prévenir les vétérinaires à proximité.
    </v-stepper-step>

    <v-stepper-content step="3">
      <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
      <v-btn color="primary" @click="e6 = 4">
        Etape suivante
      </v-btn>
      <v-btn text @click="e6 = 2">
        Etape précédente
      </v-btn>
    </v-stepper-content>

    <v-stepper-step step="4">
      Poster un message sur le groupe Facebook
      <a href="https://www.facebook.com/Filalapat/" target="_blank">
        Filalapat
      </a>
    </v-stepper-step>
    <v-stepper-content step="4">
      <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
      <v-btn color="primary" @click="e6 = 1">
        Terminer
      </v-btn>
      <v-btn text @click="e6 = 5">
        Etape précédente
      </v-btn>
    </v-stepper-content>
  </v-stepper>
</template>

<script>
import StepIcad from './steps/StepIcad'
export default {
  components: {
    StepIcad
  },
  data() {
    return {
      e6: 1
    }
  }
}
</script>
