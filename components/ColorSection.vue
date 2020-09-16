<template>
  <div class="color-top">
<div class="color-parent">
<div class="">
  NOT SURE
</div>
 <div class=""v-for="i in giveMeRange(68,76)" v-bind:key="i.id">

   {{String.fromCharCode(i)}}
 </div>
  <div class="">
    M-Z
  </div>
  <div class="">
    Fancy
  </div>
</div>
    <p class="tip">Tip: Most common center diamond color is H </p>
  </div>
</template>

<script>
export default {
name: "ColorSection",
  data(){
  return{

  }
  },
  methods:{
  giveMeRange(min,max){
    var range = []
    for(let i = min; i <= max; i++){
      range.push(i)
    }
    return range
  }

  }
}
</script>

<style scoped>
.color-top{
  width: 100%;
  height: 40vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: solid 1px black;
  border-top-style: hidden;
}
.color-parent{
  width: 90%;
  height: 75%;
  background-color: orange;
  display: grid;
  grid-template-columns: repeat(6,1fr);
  grid-template-rows: 50% 50% ;
}
.color-parent > div{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  background-color: white;
  font-size: 15px;
  flex-wrap: wrap;
  border-color:  black ;
  border-style: solid;
  border-width: 1px;
}
.tip{


}
</style>
