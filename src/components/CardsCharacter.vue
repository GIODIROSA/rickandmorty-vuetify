<template>
  <div>
    <v-container>
      <v-row>
        <v-col v-for="(personaje, index) in personajes" :key="index" cols="12" md="4">
          <v-card class="cards-character" max-width="300">
            <v-img :src="personaje.imagen" height="200px"></v-img>

            <v-card-title>
              {{ personaje.nombre }}
            </v-card-title>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn icon @click="personaje.estado = !personaje.estado ">
                <v-icon>{{
                  personaje.estado  ? "mdi-chevron-up" : "mdi-chevron-down"
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="personaje.estado">
                <v-divider></v-divider>

                <v-card-text>
                  I'm a thing. But, like most politicians, he promised more than
                  he could deliver. You won't have time for sleeping, soldier,
                  not with all the bed making you'll be doing. Then we'll go
                  with that data file! Hey, you add a one and two zeros to that
                  or we walk! You're going to do his laundry? I've got to find a
                  way to escape.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "CardsCharacter",
  data() {

    return {
      
      }
  },
 computed: {
   
   ...mapState(['personajes']),
 },
};
</script>

<style></style>
