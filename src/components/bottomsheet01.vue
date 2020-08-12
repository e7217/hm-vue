<template>
  <div class="text-center">
    <v-dialog v-model="dialog" inset scrollable max-width="600px">
      <template v-slot:activator="{ on, attrs }">
        <v-badge overlap color='orange' content="4">
        <v-btn
          color="grey"
          dark
          v-bind="attrs"
          v-on="on"
        >
          ISSUE
        </v-btn>
        </v-badge>
      </template>
      <v-sheet class="text-center" height="400px">
        <v-btn
          class="mt-6"
          text
          color="error"
          @click="sheet = false"
        >close</v-btn>
        <v-card>
            <v-card-text>
                <div class="my-3">This is a bottom sheet using the inset prop</div>
              <v-alert dense type="warning">
                    [machine01] [온도] - 설정치 초과
                  </v-alert>
              <v-alert dense type="info">
                    I'm a info alert.
                  </v-alert>
              <v-alert dense type="error">
                    I'm a error alert.
                  </v-alert>
              <v-alert dense type="warning">
                    I'm a warning alert.
                  </v-alert>
              <v-alert dense type="warning">
                    I'm a warning alert.
                  </v-alert>
              <v-alert dense type="warning">
                    I'm a warning alert.
                  </v-alert>

            </v-card-text>
        </v-card>
        
      </v-sheet>
    </v-dialog>
  </div>
</template>

<script>
  export default {
    name: "bottomsheet", 
    data: () => ({
      sheet: false,
    }),
  }
</script>