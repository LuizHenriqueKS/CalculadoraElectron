<template>
  <div class="calculadora">
    <div class="expressaoCalculo">
      {{ expressaoCalculo }}
    </div>
    <div class="valorEntrada">
      {{ valorEntrada }}
    </div>
    <TecladoCalculadora style="margin-top: 8px" @key="keyPress" />
  </div>
</template>

<script>
import TecladoCalculadora from "./TecladoCalculadora";

export default {
  components: {
    TecladoCalculadora,
  },
  data: () => ({
    expressaoCalculo: "",
    valorEntrada: "0",
  }),
};
</script>

<style scoped>
.expressaoCalculo {
  width: 100%;
  text-align: right;
  color: gray;
  padding: 4px;
  box-sizing: border-box;
  height: 24px;
}
.valorEntrada {
  width: 100%;
  font-size: 60px;
  font-weight: bold;
  text-align: right;
  padding: 4px;
  box-sizing: border-box;
}
</style>
