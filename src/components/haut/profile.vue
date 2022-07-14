<template>
  <div>
    <img alt="Vue logo" src="@/assets/marius.jpg" id="imgPrincipale" />

    <div>
      <h1>Marius Luporsi</h1>
      <h3>Software developer</h3>
      <div id="localisation">
        <img
          src="@/assets/localisation.png"
          alt="icone localisation"
          id="imgLocalisation"
        />
        <p>Nancy, France</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#imgPrincipale {
  width: 145px;
  border-radius: 50%;
}

#localisation {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: -20px;
  margin-bottom: 25px;
}

#localisation p {
  color: #4b5563;
  font-size: 12px;
}

#imgLocalisation {
  width: 20px;
  height: 20px;
}
</style>