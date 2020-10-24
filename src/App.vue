<template>
  <v-app>
    <v-card color="grey lighten-4" flat height="80px" tile>
      <v-toolbar dense>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-toolbar-title>Mi App</v-toolbar-title>

        <v-spacer></v-spacer>
        <v-btn text>
          <span>iNICIO</span>
        </v-btn>

        <v-btn text>
          <span>BUSCAR</span>
        </v-btn>

        <v-btn text>
          <span>ACERCA DE</span>
        </v-btn>
      </v-toolbar>
    </v-card>

    <v-main>
      <v-container>
        <v-row>
          <v-col md="4" v-for="(personaje, i) in personajes" :key="i">
            <v-card class="mx-auto" max-width="300">
              <v-img
                class="white--text align-end"
                height="200px"
                :src="personaje.imagen"
              >
              </v-img>

              <v-card-title class="pb-0"> {{ personaje.nombre }} </v-card-title>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-card height="50">
      <v-footer absolute class="font-weight-medium">
        <v-col class="text-center" cols="12">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-col>
      </v-footer>
    </v-card>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    personajes: [
      {
        id: 1,
        nombre: "Morty",
        imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
      },
      {
        id: 2,
        nombre: "Rick",
        imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
      },
      {
        id: 3,
        nombre: "Summer",
        imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
      },
      {
        id: 4,
        nombre: "Beth",
        imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
      },
      {
        id: 5,
        nombre: "Jerry",
        imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
      },
    ],
  }),
};
</script>
