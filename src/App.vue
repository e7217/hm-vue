<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />
      <div class="text-h6">HM MACHINE STATUS MONITOR</div>

        <!-- <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        /> -->
      </div>


      <v-spacer></v-spacer>

        
      <bottomsheet class="mr-4"/>
      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
      
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container fluid>
        <v-row
        class = "mb-4">
        <v-col v-for="n in 12" :key="n">
      <comp01 class="ma-2"/>

        </v-col>
        </v-row>
      </v-container>
  

      <!-- <bottomsheet/> -->
      <!-- <HelloWorld/> -->
      
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import comp01 from './components/comp01';
import bottomsheet from './components/bottomsheet01';

export default {
  name: 'App',

  components: {
    bottomsheet,
    // HelloWorld,
    comp01,

  },

  data: () => ({
    //
  }),
};
</script>
