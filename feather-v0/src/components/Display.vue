<template>
  <div class="screen"></div>
</template>

<script>
export default {};
</script>

<style>
.screen {
  border: 1px solid #ff5c5c;
  border-radius: 10px;
  height: 542px;
  /* width: 1192px; */
  /* margin-left: 30px; */
}
@media only screen and (max-width: 700px) {
  .screen {
    margin-top: 30px;
    margin-left: 0px;
    width: 100%;
  }
}
@media only screen and (min-width: 701px) {
  .screen {
    margin-left: 30px;
    width: 1192px;
  }
}
</style>