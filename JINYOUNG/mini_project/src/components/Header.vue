<template>
  <nav>
    <v-app-bar app dark>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <div class="d-flex align-center">
        <v-btn class="logo" :ripple="false" @click="moveHome">
          <v-img src="@/assets/logo.png" width="100" />
        </v-btn>
      </div>

      <v-spacer></v-spacer>

      <v-btn :ripple="false" href="https://github.com/leejinzero/Vue_Study" text>
        <span class="mr-2">GitHub</span>
        <v-icon>mdi-git</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer app dark v-model="drawer" temporary>
      <v-list>
        <v-list>
          <v-list-item v-for="item in links" :key="item.text" :to="item.route">
            <v-list-item-content>
              <v-list-item-title v-html="item.text"></v-list-item-title>
            </v-list-item-content>

            <v-list-item-action>
              <v-icon style="color:white">{{ item.icon }}</v-icon>
            </v-list-item-action>
          </v-list-item>
        </v-list>

        <v-divider></v-divider>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  methods: {
    moveHome() {
      this.$router.push("/");
    }
  },
  data() {
    return {
      drawer: false,
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

<style scoped>
.logo--contained {
  box-shadow: none;
}

.logo:not(.v-btn--text):not(.v-btn--outlined):hover:before,
.theme--dark.logo:hover::before {
  opacity: 0;
}
</style>
