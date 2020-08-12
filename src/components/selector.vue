<template>
    <v-select 
    align="center"
    label="select"
    :items="items"
    dense
    outlined
    >
    </v-select>
</template>

<script>
  export default {
    name: "selector", 
    data: () => ({
        items:['select01', 'select02', 'select03', 'select04'],
    }),
  }
</script>