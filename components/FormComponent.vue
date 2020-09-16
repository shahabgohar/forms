<template>
  <div class="parent">
    <div class="form-heading">
      <p>DESCRIBE YOUR RING</p>
    </div>
  <sections-component name="Settings" @displaySection = "displayPrticular" @closeSection = "closeParticular" id="0"></sections-component>
    <settings-section-component v-if="this.sections[0]"></settings-section-component>
    <sections-component name="Shape" @displaySection = "displayPrticular" @closeSection = "closeParticular" id="1"></sections-component>
    <shape-section v-if="this.sections[1]"></shape-section>
    <sections-component name="Carat Weight" @displaySection = "displayPrticular" @closeSection = "closeParticular" id="2"></sections-component>
    <carat-section v-if="this.sections[2]"></carat-section>
    <sections-component name="Color" @displaySection = "displayPrticular" @closeSection = "closeParticular" id="3"></sections-component>
    <color-section v-if="this.sections[3]"></color-section>
    <sections-component name="Clarity" @displaySection = "displayPrticular" @closeSection = "closeParticular" id="4"></sections-component>
    <clarity-component v-if="this.sections[4]"></clarity-component>
    <sections-component name="Grading Lab Certificate" style="border-bottom-style: solid" @displaySection = "displayPrticular" @closeSection = "closeParticular" id="5"></sections-component>
    <grading-lab  v-if="this.sections[5]"></grading-lab>
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
    show:false,
    sections:[]
  }
  },
  mounted() {
  for (let i = 65;i<70;i++){
    this.sections.push(false)
  }
  },
  methods:{
    displayPrticular(i){
      console.log(i)
    this.sections[i] = true
      this.$forceUpdate()
    },
    closeParticular(i){
      this.sections[i] = false
      this.$forceUpdate()
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
