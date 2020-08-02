<template>
  <v-list>
    <v-list>
      <v-list-item v-for="item in links" :key="item.text" :to="item.route">
        <v-list-item-content>
          <v-list-item-title v-html="item.text"></v-list-item-title>
        </v-list-item-content>

        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>
  </v-list>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { text: "Home", icon: "mdi-home", route: "/" },
        { text: "Home", icon: "mdi-home" },
        { text: "Home", icon: "mdi-home" },
        { text: "Home", icon: "mdi-home" },
        { text: "Home", icon: "mdi-home" }
      ]
    };
  }
};
</script>

<style>
</style>