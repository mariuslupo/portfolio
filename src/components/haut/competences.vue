<template>
  <div class="competence">
    <p>Python</p>
    <p>VueJS</p>
    <p>Machine learning</p>
    <p>Flutter</p>
    <!-- <p>NodeJS</p> -->
  </div>
</template>

<script>
export default {};
</script>

<style>
.competence {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.competence p {
  background: #eff6ff;
  border-radius: 25px;
  color: #1e40ef;
  padding-left: 10px;
  padding-right: 10px;
  font-size: 14px;
  font-weight: bold;
}
</style>