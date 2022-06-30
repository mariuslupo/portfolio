<template>
  <div id="page">
    <div id="haut">
      <img alt="Vue logo" src="./assets/marius.jpg" id="imgPrincipale" />
      <div>
        <h1>Marius Luporsi</h1>
        <h3>Software developer</h3>
      </div>
      <div id="social">
        <a
          href="https://www.linkedin.com/in/marius-luporsi-a637771a2/"
          target="_blank"
        >
          <img alt="LinkedIn logo" src="./assets/linkedin.png" />
        </a>
        <a href="https://github.com/mariuslupo" target="_blank">
          <img alt="Github logo" src="./assets/github.png" />
        </a>
        <a href="https://www.kaggle.com/marius9991" target="_blank">
          <img alt="Kaggle logo" src="./assets/kaggle.png" id="kaggle" />
        </a>
      </div>
    </div>
    <div id="bas">
      <h2>Projects</h2>
      <div id="listeProjets">
        <div class="projet" v-for="x in projets" :key="x.Titre">
          <div class="imageProject">
            <a :href="x.Lien" target="_blank">
              <img alt="Lien logo" src="./assets/cover.jpg" />
            </a>
          </div>
          <div id="textProject">
            <h3>{{ x.Titre }}</h3>
            <p>{{ x.Description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  data() {
    return {
      projets: [
        {
          Titre: "Projet 1",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 1",
          Image: "./assets/projet1.png",
        },
        {
          Titre: "Projet 2",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 2",
          Image: "./assets/projet2.png",
        },
        {
          Titre: "Projet 3",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 3",
          Image: "./assets/projet3.png",
        },
        {
          Titre: "Projet 4",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 4",
          Image: "./assets/projet4.png",
        },
        {
          Titre: "Projet 5",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 5",
          Image: "./assets/projet5.png",
        },
        {
          Titre: "Projet 6",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 6",
          Image: "./assets/projet6.png",
        },
        {
          Titre: "Projet 7",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 7",
          Image: "./assets/projet7.png",
        },
        {
          Titre: "Projet 8",
          Description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          Lien: "Lien du projet 8",
          Image: "./assets/projet8.png",
        },
      ],
    };
  },
  components: {
    // HelloWorld
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
  /* background-color: #8d9eae; */
  width: 100%;
  height: 375px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

#bas {
  background-color: #f9fafb;
  width: 100%;
  padding-top: 20px;
}

#imgPrincipale {
  width: 145px;
  border-radius: 50%;
}

#haut h3 {
  margin-top: -15px;
  /* margin-bottom: 15px; */
}

#bas h2 {
  text-align: start;
  margin-left: 6.5%;
}

#social {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

#social img {
  width: 25px;
  height: 25px;
}

#kaggle {
  width: 35px !important;
}

.projet {
  width: 40%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 45px;
  background: #fff;
}

#listeProjets {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

#listeProjets img {
  width: 100%;
  height: 150px;
  object-fit: fill;
  border-top-right-radius: 15px;
  border-top-left-radius: 15px;
}

.imageProject {
  width: 100%;
}

#textProject {
  padding: 15px;
  text-align: left;
}
</style>
