<template>
  <div id="social">
    <a
      href="https://www.linkedin.com/in/marius-luporsi-a637771a2"
      target="_blank"
    >
      <img alt="LinkedIn logo" src="@/assets/linkedin.png" />
    </a>
    <a href="https://github.com/mariuslupo" target="_blank">
      <img alt="Github logo" src="@/assets/github.png" />
    </a>
    <a href="https://www.kaggle.com/marius9991" target="_blank">
      <img alt="Kaggle logo" src="@/assets/kaggle.png" id="kaggle" />
    </a>
    <!-- <a href="https://www.kaggle.com/marius9991" target="_blank">
          <img alt="CV logo" src="./assets/cv.png"/>
        </a> -->
  </div>
</template>

<script>
export default {};
</script>

<style>
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
</style>