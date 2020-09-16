<template>
  <div style="width: 100%; height: 25vh; border: solid 1px black;
  border-top-style: hidden;">
<div class="grading">
  <div class="labs">
  <div class="">

    <p>NONE</p>

  </div>
  <div class="">

    <p>GIA</p>

  </div>
  <div class="" style="border-right-style: hidden">

    <p>IGI,GS1 OR OTHER</p>

</div>
  </div>
  </div>
  </div>
</template>

<script>
export default {
name: "GradingLab"
}
</script>

<style scoped>
.grading{
  margin-bottom: 2%;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

}
.grading > .labs{
width: 80%;
  height: 60%;
  display: grid;
  grid-template-columns: repeat(3,33.33%);
  grid-template-rows: 100%;
  border: solid 1px black;

}
.labs > div{
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  border-right-style: solid;
  border-right-color: black;
  border-right-width: 1px;
}
.labs > div > p{
  font-size: 25px;
}

</style>
