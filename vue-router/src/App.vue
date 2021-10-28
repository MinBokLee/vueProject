<template>
  <v-app id="inspire">
    <the-drawer :drawer="drawer" />
    <the-header :drawerOpenHandler="drawerOpenHandler" />
    <v-content>
      <router-view></router-view>
    </v-content>
    <the-footer />
  </v-app>
</template>

<script>
import TheHeader from "@/layout/TheHeader.vue";
import TheFooter from "@/layout/TheFooter.vue";
import TheDrawer from "@/layout/TheDrawer.vue";
export default {
  components: {
    TheHeader,
    TheFooter,
    TheDrawer,
  },

  data() {
    return {
      drawer: false,
    };
  },
  props: {
    source: String,
  },
  methods: {
    test() {
      alert("클릭");
    },
    drawerOpenHandler() {
      this.drawer = !this.drawer;
    },
  },
};
</script>
