<template>
  <div id="app">
    <MyAccordion/>
  </div>
</template>

<script>
import MyAccordion from "@/components/MyAccordion";

export default {
  name: "App",
  components: {
    MyAccordion,
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
