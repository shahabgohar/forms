<template>
<div class="counter">
  <div class="count">
    <div class="count-1">
      <div class="number">1</div>
    </div>
    <div class="line"></div>
    <div class="count-1">
      <div class="number">2</div>
    </div>
    <div class="line"></div>
    <div class="count-1">
      <div class="number">3</div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "FormCounter"
}
</script>

<style scoped>
.counter{
  width: 100%;
  height: 15vh;
  background-color: whitesmoke;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.count{
  width: 40%;
  height: 100%;
  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: space-around;
}
.count-1{

  width: 10%;
  height: 50%;
 background-image: url("/svg/circle.svg");
  background-repeat: no-repeat;
  background-position: center;
  position: relative;
}
.number{
  position: absolute;
 width: 85%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #F5F5F5;
}
.line{
  width: 30%;
  height: 4%;
  background-image: url("/svg/line.svg");
  background-repeat: no-repeat;
  background-position: center;
}
</style>
