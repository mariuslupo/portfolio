<template>
  <div class="projet" @click="redirect(Lien)">
    <div class="imageProject">
      <img alt="Lien logo" :src="require(`../../assets/${Image}.jpg`)" />
    </div>
    <div id="textProject">
      <h3>{{ Titre }}</h3>
      <p>{{ Description }}</p>
    </div>
    <div class="competence competenceProject">
      <p v-for="y in Competence" :key="y.name">{{ y }}</p>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    redirect(lien) {
      window.open(lien, "_blank");
    },
  },
  props: ["Titre", "Lien", "Description", "Competence", "Image"],
};
</script>

<style>
.projet {
  display: flex;
  flex-direction: column;
  /* align-items: center;
  justify-content: space-between; */
  margin-top: 10px;
  margin-bottom: 30px;
  background: #fff;
  cursor: pointer;
  transition: transform 0.3s;
  overflow: hidden;
  border-radius: 10px 10px 0 0;
}

.projet:hover {
  transform: scale(1.05);
}

.imageProject {
  width: 100%;
}

#textProject {
  padding: 15px;
  padding-top: 0;
  padding-bottom: 0;
  text-align: left;
}

.competenceProject {
  width: 100%;
  justify-content: left !important;
  margin-left: 15px;
  flex-wrap: wrap;
  margin-bottom: 5px;
  margin-top: auto;
}

@media screen and (max-width: 768px) {
  .projet {
    width: 90%;
  }
}

@media screen and (min-width: 768px) {
  .projet {
    width: 40%;
  }
}
</style>