<template>
<v-badge overlap color='orange' content="2">
<v-hover >
    <template v-slot:default="{ hover }">
  <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
  
    <!-- <v-list-item three-line>
      <v-list-item-content>
        <div class="overline mb-4">사출기A</div>
        <v-list-item-title class="headline mb-1">Headline 5</v-list-item-title>
        <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
      </v-list-item-content>



      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item> -->

    <!-- <v-card-actions>
      <v-btn href="https://www.naver.com" text> 제어 </v-btn>
      <v-btn text>Button</v-btn>
    </v-card-actions> -->
    <div class="text-h8 ma-2">Molding Machine A</div>
    <div class="text-h6 ml-2 mb-4">Temperature Controller</div>
    <v-data-table
        :headers="headers"
        :items="dataset01"
        hide-default-footer
        class="elevation-1"
    >
        <template v-slot:item.value="{ item }">
        <v-chip :color="getColor(item.value)" dark>{{ item.value }}</v-chip>
        </template>
    </v-data-table>

    <v-fade-transition>
      <v-overlay
        v-if="hover"
        absolute
        color="#036358"
      >
      
        <v-btn class="ma-2" href="http://www.naver.com">Control</v-btn>
        <v-btn class="ma-2" href="http://www.google.com">Detail</v-btn>
      </v-overlay>
    </v-fade-transition>
        </v-card>
    </template>
  </v-hover>
</v-badge>
</template>

<script>
export default {
    name: 'comp01',
    data: () => ({
        overlay: false,
        headers: [
            {
            text: 'Parameter',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'value', value: 'value' },
        ],
        dataset01: [
            {
                name: "Temperature01",
                value: 45
            },
            {
                name: "Temperature02",
                value: 27.4
            },
            {
                name: "Temperature03",
                value: 35
            },
            {
                name: "Temperature04",
                value: 11
            },
        ],
        dataset02:[
            {
            machine:"machine01",
            type:"fp"
            },
            {
            machine:"machine02",
            type:"fp"
            },
            {
            machine:"machine03",
            type:"fp"
            },
                     
        ]        
    }),
    methods: {
        getColor (value) {
        if (value > 40) return 'red'
        else if (value < 20) return 'blue'
        else return 'green'
      },
    },
}
</script>