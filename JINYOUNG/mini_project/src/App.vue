<template>
  <v-app>
    <Header />
    <v-main>
      <aside>
        <Sidebar />
      </aside>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Sidebar from "./components/Sidebar";

export default {
  name: "App",

  components: {
    Header,
    Sidebar
  },

  data: () => ({
    //
  })
};
</script>
<style scoped>
aside {
  position: fixed;
  width: 10%;
  padding-left: 15px;
  margin-left: 15px;
  float: left;
}
</style>
