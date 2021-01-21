<template>
  <q-layout view="lHh Lpr lFf">
    <Header />
    <q-page-container class="contt">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import Header from "../components/Header";

export default {
  name: "MainLayout",
  components: { Header },
  data() {
    return {};
  }
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
a {
  text-decoration: none;
}
body {
  background: #161623;
  position: relative;
}
body::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(#f00, #f0f);
  clip-path: circle(30% at 50% 100%);
}
body::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(#2196f3, #e91e63);
  clip-path: circle(20% at 10% 10%);
}
</style>
