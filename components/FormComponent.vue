<template>
  <div class="parent">
    <div class="form-heading">
      <p>DESCRIBE YOUR RING</p>
    </div>
  <sections-component></sections-component>
    <settings-section-component></settings-section-component>
    <sections-component></sections-component>
    <shape-section></shape-section>
    <sections-component></sections-component>
    <carat-section></carat-section>
    <sections-component></sections-component>
    <color-section></color-section>
    <sections-component></sections-component>
    <clarity-component></clarity-component>
    <sections-component></sections-component>
    <grading-lab></grading-lab>
    <div class="button-submit">
      <button>Continue</button>
    </div>
    <div class="button-submit center">
      <p>Need Help ? </p> <a style="padding-left: 2%" href=""> Click here !</a>
    </div>
  </div>
</template>
<script>
import SettingsSectionComponent from "~/components/SettingsSectionComponent";
import ShapeSection from "~/components/ShapeSection";
import SectionsComponent from "~/components/SectionsComponent";
import CaratSection from "@/components/CaratSection";
import ColorSection from "@/components/ColorSection";
import ClarityComponent from "@/components/ClarityComponent";
import GradingLab from "@/components/GradingLab";
export default {
name:"FormComponent",
  components: {
    GradingLab,
    ClarityComponent, ColorSection, CaratSection, SectionsComponent, ShapeSection, SettingsSectionComponent},
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
  width: 50%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-evenly;
}

.form-heading{
  width: 100%;
  height: 20vh;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.form-heading > p{
  font-size: 40px;
}
.button-submit{
  width: 100%;
  height: 10vh;
  padding-top: 5%;
}
.button-submit > button{
  width: 100%;
  height: 100%;
  background-color: #7F828B;
  font-size: 40px;
}
.center{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.center > p{
  font-size: 30px;
}
.center > a{
  font-size: 30px;
}

</style>
