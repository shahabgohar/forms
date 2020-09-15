<template>
  <div class="parent-all">
<form-counter></form-counter>
    <form-component></form-component>
  </div>
</template>

<script>
import FormCounter from "~/components/FormCounter";
import FormComponent from "~/components/FormComponent";
export default {
  components: {FormComponent, FormCounter}
}
</script>
<style scoped>
.parent-all{
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
</style>

