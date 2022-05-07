<template>
  <v-toolbar color="indigo" dark fixed app>
  </v-toolbar>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      menu: [
        { icon: "home", title: "Link A" },
        { icon: "info", title: "Link B" },
        { icon: "warning", title: "Link C" },
      ],
    };
  },

  methods: {
    menuItems() {
      return this.menu;
    },
  },
};
</script>