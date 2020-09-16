<template>
  <div class="caret-top">
<div class="carat-parent">
<div class="input-carat">
  <input type="text">
</div>
  <div class="carat-image" >

  </div>

</div>
    <div style="width: 100%; height: 10%">
    <p>Tip : The most common is</p>
    </div>
  </div>

</template>

<script>
export default {
name: "CaratSection"
}
</script>

<style scoped>
.caret-top{
  width: 100%;
  height: 40vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: solid 1px black;
  border-top-style: hidden;
}
.carat-parent{
  height: 70%;
  width: 100%;
  display: grid;
  grid-template-columns:  20% 80%;
  grid-template-rows: 100%;
}
.input-carat{
display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

}
.input-carat > input{
  width: 40%;
  height: 25%;
  padding: 10% 15%;
  font-size: 30px;
}
.carat-image{
  background-image: url("/images/carat.png");
  background-repeat: no-repeat;
   background-position :right top;
  background-size: cover;
}
p{
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: black;
}
@media screen and (max-width: 1200px){

}
</style>
