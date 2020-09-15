<template>
  <div class="parent">
    <div class="sections">
      <div class="svg-holder" style="padding-right: 50%">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 21.64 15.96"><defs><style>.tick{fill:none;stroke:#cccc31;stroke-miterlimit:10;}</style></defs><title>tick</title><g><polyline class="tick" points="0.44 6.91 4.91 15.16 21.31 0.37"/></g></svg>
      </div>
        <p @click="showDetails()">Settings</p>
      <div class="svg-holder">
        <svg v-if="show" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10.45 6.16"><defs><style>.dropdown-up-arrow{fill:none;stroke:#000;stroke-miterlimit:10;}</style></defs><title>up-arrow</title><g><polyline class="dropdown-up-arrow" points="0.33 5.38 5.75 0.71 10.07 5.83"/></g></svg>
        <svg v-if="!show" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10.56 6.26"><defs><style>.dropdown-up-arrow{fill:none;stroke:#000;stroke-miterlimit:10;}</style></defs><title>down-arrow</title><g ><polyline class="dropdown-up-arrow" points="0.38 0.33 4.9 5.57 10.24 1.13"/></g></svg>
      </div>
    </div>
    <settings-section-component v-if="this.show"></settings-section-component>
    <div class="sections">
      <div class="svg-holder" style="padding-right: 50%">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 21.64 15.96"><defs><style>.tick{fill:none;stroke:#cccc31;stroke-miterlimit:10;}</style></defs><title>tick</title><g><polyline class="tick" points="0.44 6.91 4.91 15.16 21.31 0.37"/></g></svg>
      </div>
      <p @click="showDetails()">Settings</p>
      <div class="svg-holder">
        <svg v-if="show" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10.45 6.16"><defs><style>.dropdown-up-arrow{fill:none;stroke:#000;stroke-miterlimit:10;}</style></defs><title>up-arrow</title><g><polyline class="dropdown-up-arrow" points="0.33 5.38 5.75 0.71 10.07 5.83"/></g></svg>
        <svg v-if="!show" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10.56 6.26"><defs><style>.dropdown-up-arrow{fill:none;stroke:#000;stroke-miterlimit:10;}</style></defs><title>down-arrow</title><g ><polyline class="dropdown-up-arrow" points="0.38 0.33 4.9 5.57 10.24 1.13"/></g></svg>
      </div>
    </div>
    <shape-section></shape-section>
  </div>
</template>
<script>
import SettingsSectionComponent from "~/components/SettingsSectionComponent";
import ShapeSection from "~/components/ShapeSection";
export default {
name:"FormComponent",
  components: {ShapeSection, SettingsSectionComponent},
  data(){
  return{
    show:false
  }
  },
  methods:{
    showDetails(){
      this.show = !this.show
    }
  }
}
</script>
<style scoped>
.parent{
  width: 60%;
  height: fit-content;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: stretch;
}
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
</style>
