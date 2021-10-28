<template>
  <v-toolbar color="indigo" dark fixed app>
    <v-toolbar-side-icon @click="drawerOpenHandler"></v-toolbar-side-icon>
    <v-toolbar-title>Application</v-toolbar-title>
  </v-toolbar>
</template>
<script>
export default {
  name: "TheHeader",
  props: {
    drawerOpenHandler: {
      type: Function,
    },
  },
};
</script>
