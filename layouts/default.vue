<template>
  <div>
    <nav-bar-component></nav-bar-component>
    <Nuxt />
  </div>
</template>

<script>
import NavBarComponent from "~/components/NavBarComponent";
export default {
  components: {NavBarComponent}
}
</script>
