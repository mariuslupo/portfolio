<template>
  <div id="page">
    <div id="haut">
      <profile />
      <social />
      <competence />
    </div>
    <div id="bas">
      <h2>Projects</h2>
      <div id="listeProjets">
        <projet
          v-for="x in mesProjets"
          :key="x.Titre"
          :Titre="x.Titre"
          :Lien="x.Lien"
          :Description="x.Description"
          :competence="x.competence"
        />
      </div>
    </div>
  </div>
</template>

<script>
import profile from "./components/haut/profile.vue";
import social from "./components/haut/social.vue";
import competence from "./components/haut/competences.vue";
import projet from "./components/bas/projets.vue";
import { mesProjets } from "./data.js";

export default {
  name: "App",
  data() {
    return {
      mesProjets: mesProjets,
    };
  },
  components: {
    profile,
    social,
    competence,
    projet,
  },
};
</script>

<style>
html,
body {
  height: 100vh;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
}

p {
  line-height: 1.8;
  text-align: left;
  word-wrap: break-word;
}

#haut {
  width: 100%;
  height: 425px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

#bas {
  background-color: #f9fafb;
  width: 100%;
  padding-top: 10px;
}

#haut h3 {
  margin-top: -15px;
}

#bas h2 {
  text-align: start;
  margin-left: 6.5%;
}
</style>
