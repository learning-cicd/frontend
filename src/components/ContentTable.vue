<template>
    <v-card>
    <v-card-title>
    <v-btn elevation="2">Print Table</v-btn>
    <v-btn elevation="2">Print forms</v-btn>
    <v-btn elevation="2">Export to Excel</v-btn>
    <v-btn elevation="2">Import from Excel</v-btn>
    <v-btn elevation="2">Column Visibility</v-btn>
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      v-model="selected"  
      :headers="headers"
      :items="desserts"
      :search="search"
      :single-select="singleSelect"
      item-key="name"
      show-select
    >
    
    <template v-slot:[`item.actions`]="{ item }">
      <v-icon
        small
        class="mr-2"
        @click="editItem(item)"
      >
        mdi-pencil
      </v-icon>
      <v-icon
        small
        @click="deleteItem(item)"
      >
        mdi-delete
      </v-icon>
    </template>
    <template v-slot:no-data>
      <v-btn
        color="primary"
        @click="initialize"
      >
        Reset
      </v-btn>
    </template></v-data-table>
    </v-card>
</template>

<script>
import Vuetify from 'vuetify'
export default {
  name: 'ContentTable',
  props: {
  },
  vuetify: new Vuetify(),
  data () {
    return {
      selected : [],
      singleSelect : false,
      headers: [
        { text: 'Actions', value: 'actions', sortable: false },
        { text: 'MaterialCode', value: 'calories' },
        { text: 'Submission No.', value: 'fat' },
        { text: 'Image', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
        { text: 'MaterialCode', value: 'calories' },
        { text: 'Submission No.', value: 'fat' },
        { text: 'Image', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
        { text: 'MaterialCode', value: 'calories' },
        { text: 'Submission No.', value: 'fat' },
        { text: 'Image', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
        { text: 'MaterialCode', value: 'calories' },
        { text: 'Submission No.', value: 'fat' },
        { text: 'Image', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
      ],
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%',
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%',
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7%',
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8%',
        },
        {
          name: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: '16%',
        },
        {
          name: 'Jelly bean',
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: '0%',
        },
        {
          name: 'Lollipop',
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: '2%',
        },
        {
          name: 'Honeycomb',
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: '45%',
        },
        {
          name: 'Donut',
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: '22%',
        },
      ],
    }
  },
}
</script>


