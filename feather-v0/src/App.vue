<template>
  <div class="cont">
    <Sidebar />
    <Display />
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar.vue";
import Display from "./components/Display.vue";
export default {
  components: { Sidebar },
  setup() {
    return {
      Sidebar,
      Display,
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter&display=swap");
body {
  background: #292929;
  /* margin: 90px 60px 90px 60px; */
  padding: 0;
  box-sizing: border-box;
  font-family: Inter;
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: 15px;
  letter-spacing: 0em;
  text-align: left;
}
/* small */
@media only screen and (max-width: 700px){
  body{
    margin: 60px 15px 60px 15px;
  }
  .cont{
    display: inline;
  }
}
/* large */
@media only screen and (min-width: 701px) {
  .cont{
    display: flex;
  }
  body {
    margin: 90px 60px 90px 60px;
  }
}
</style>
