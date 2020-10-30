<template>
  <div class="tecladoCalculadora">
    <div>%</div>
    <div>CE</div>
    <div>C</div>
    <div>B</div>

    <div>1/x</div>
    <div>X²</div>
    <div>R²</div>
    <div>D</div>

    <div class="corClara" @click="keyPress('7')">7</div>
    <div class="corClara" @click="keyPress('8')">8</div>
    <div class="corClara" @click="keyPress('9')">9</div>
    <div>x</div>

    <div class="corClara" @click="keyPress('6')">6</div>
    <div class="corClara" @click="keyPress('5')">5</div>
    <div class="corClara" @click="keyPress('4')">4</div>
    <div>-</div>

    <div class="corClara" @click="keyPress('3')">3</div>
    <div class="corClara" @click="keyPress('2')">2</div>
    <div class="corClara" @click="keyPress('1')">1</div>
    <div>+</div>

    <div class="corClara">+/-</div>
    <div class="corClara" @click="keyPress('0')">0</div>
    <div class="corClara">,</div>
    <div class="corAzulClaro">=</div>
  </div>
</template>

<script>
export default {
  props: {
    msg: String,
  },
  methods: {
    keyPress(key) {
      this.$emit("keyPress", { key });
    },
  },
};
</script>

<style scoped>
.tecladoCalculadora {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}
.tecladoCalculadora > div {
  background-color: #e0e0e0;
  margin: 1px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-size: 17px;
}
.tecladoCalculadora > div:hover {
  box-shadow: inset 86px 0px 0px 20px #00000010;
}
.tecladoCalculadora > div:active {
  box-shadow: inset 86px 0px 0px 20px #00000033;
}
div.corClara {
  background-color: #eeeeee;
}
div.corAzulClaro {
  background-color: #5296dda6;
}
</style>
