<template>
  <div>
    <div class="logo">
      <img src="../assets/logo.svg" />
    </div>
    <div class="opt">
      <div v-for="(i, j) in state.simulatable" :key="i" :for="j">
        <input
          class="sel"
          type="radio"
          v-bind:key="j"
          :value="i"
          :id="j"
          name="o"
          v-model="state.simThis"
        />
        <label class="lab" v-bind:for="j">{{ i }}</label>
      </div>
    </div>
    <br />
    <!-- <span>{{ state.simThis }}</span> -->
    <button class="play" @click="printThis()">
      <svg
        width="9"
        height="12"
        viewBox="0 0 9 12"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M8 6L1.33333 1L1.33333 11L8 6Z"
          fill="#292929"
          stroke="#292929"
          stroke-linejoin="round"
        />
      </svg>
    </button>
  </div>
</template>

<script>
import { reactive } from "vue";
export default {
  setup() {
    const state = reactive({
      simThis: "HIV Molecule",
      c: 0,
      simulatable: {
        one: "HIV Molecule",
        two: "COVID Molecule",
        three: "Hydrogen",
        four: "Helium",
        five: "Cesium",
        six: "Unobtainium",
      },
    });
    function printThis() {
      return state.simThis;
    }
    return {
      state,
      printThis,
    };
  },
};
</script>

<style scoped>
.logo {
  height: 60px;
  width: 160px;
  display: grid;
  place-items: center;
  border: 1px solid #ff5c5c;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}
.opt {
  height: auto;
  width: 160px;
  border: 1px solid #ff5c5c;
  background-color: #ff5c5c;
  color: #292929;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  overflow-y: none;
}
.opt *,
.opt *:hover,
.opt *:after {
  box-sizing: border-box;
}
.sel {
  display: none;
}
.lab {
  display: grid;
  grid-template-columns: max-content auto;
  height: 30px;
  place-items: center;
  padding-left: 15px;
  border-radius: 0px;
}
.lab:hover {
  background-color: #292929;
  color: #ff5c5c;
  border: none;
  border-radius: 10px;
  transition: 150ms ease-in-out;
}
input[type="radio"]:checked + label {
  background: #292929;
  color: #ff5c5c;
  border-radius: 10px;
  transition: 150ms ease-in-out;
}
button {
  height: 30px;
  width: 160px;
  border-radius: 10px;
  background: #ff5c5c;
  border: none;
}
button:hover {
  background-color: #292929;
  color: #ff5c5c;
  border: 1px solid #ff5c5c;
  transition: 150ms ease-in-out;
}
button:hover > svg > path {
  fill: #ff5c5c;
  stroke: #ff5c5c;
}
</style>