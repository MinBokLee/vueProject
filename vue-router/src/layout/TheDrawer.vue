<template>
  <v-navigation-drawer v-model="draw" fixed app>
    <v-list dense>
      <v-list-tile router :to="{ name: 'home' }" exact>
        <v-list-tile-action>
          <i class="fas fa-home"></i>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Home</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile router :to="{ name: 'about-name' }" exact>
        <v-list-tile-action>
          <i class="fas fa-user"></i>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>About</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile
        router
        :to="{
          name: 'users',
          params: {
            userId: 4321,
            name: 'hoza',
          },
          query: {
            group: 'member',
            category: 'trial',
          },
        }"
        exact
      >
        <v-list-tile-action>
          <i class="fas fa-home"></i>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Users</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
</template>
<script>
export default {
  props: {
    drawer: {
      type: Boolean,
      required: true,
    },
  },
  computed: {
    draw: {
      get() {
        return this.drawer;
      },
      set(val) {
        this.$emit("openclose", val);
      },
    },
  },
};
</script>
