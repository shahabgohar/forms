<template>
  <div class="sections">
    <div class="svg-holder" style="padding-right: 50%">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 21.64 15.96"><defs><style>.tick{fill:none;stroke:#cccc31;stroke-miterlimit:10;}</style></defs><title>tick</title><g><polyline class="tick" points="0.44 6.91 4.91 15.16 21.31 0.37"/></g></svg>
    </div>
    <p @click="tellParentToShow()">{{name}}</p>
    <div class="svg-holder">
      <svg v-if="isShowing" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10.45 6.16"><defs><style>.dropdown-up-arrow{fill:none;stroke:#000;stroke-miterlimit:10;}</style></defs><title>up-arrow</title><g><polyline class="dropdown-up-arrow" points="0.33 5.38 5.75 0.71 10.07 5.83"/></g></svg>
      <svg v-if="!isShowing" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10.56 6.26"><defs><style>.dropdown-up-arrow{fill:none;stroke:#000;stroke-miterlimit:10;}</style></defs><title>down-arrow</title><g ><polyline class="dropdown-up-arrow" points="0.38 0.33 4.9 5.57 10.24 1.13"/></g></svg>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionsComponent",
  props:['name','id'],
  data(){
    return {
      isShowing:false
    }
  },
  methods:{
    tellParentToShow(){
      if(this.isShowing){
        this.$emit("closeSection",this.id)
        this.isShowing = false
      }else{
        this.$emit("displaySection",this.id)
        this.isShowing = true
      }

    }
  }
}
</script>

<style scoped>
.sections{
  width: 100%;
  height: 10vh;
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  border-style: solid;
  border-width: 1px;
  border-color: black;
  border-bottom-style: hidden;
  justify-content: start;
}
.sections > p{
  justify-self: start;
  align-items: center;
  font-size: 25px;
}
.svg-holder{
  justify-self: end;
  align-self: center;
  width: 20%;
  height: 50%;
  margin-right: 5%;
}
@media screen and (max-width: 1200px) {
  .sections{
    width: 100%;
    height: 5vh;
    display: grid;
    grid-template-columns: 15% 70% 15%;
    border-style: solid;
    border-width: 1px;
    border-color: black;
    border-bottom-style: hidden;
    justify-content: start;
  }
}
@media screen and (min-width: 290px) and (max-width: 725px){
  .sections > p{
    justify-self: start;
    align-items: center;
    font-size: 10px;
  }
}
</style>
