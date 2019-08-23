<template>
  <div class="calculator">
    <Display value="10000" />
    <Button triple label="AC" @onCalcButtonClick="clearMemory" />
    <Button operation label="/" @onCalcButtonClick="setOperation" />
    <Button label="7" @onCalcButtonClick="addDigit" />
    <Button label="8" @onCalcButtonClick="addDigit" />
    <Button label="9" @onCalcButtonClick="addDigit" />
    <Button operation label="x" @onCalcButtonClick="setOperation" />
    <Button label="4" @onCalcButtonClick="addDigit" />
    <Button label="5" @onCalcButtonClick="addDigit" />
    <Button label="6" @onCalcButtonClick="addDigit" />
    <Button operation label="-" @onCalcButtonClick="setOperation" />
    <Button label="1" @onCalcButtonClick="addDigit" />
    <Button label="2" @onCalcButtonClick="addDigit" />
    <Button label="3" @onCalcButtonClick="addDigit" />
    <Button operation label="+" @onCalcButtonClick="setOperation" />
    <Button double label="0" @onCalcButtonClick="addDigit" />
    <Button label="." @onCalcButtonClick="addDigit" />
    <Button label="=" operation @onCalcButtonClick="setOperation" />
  </div>
</template>

<script>
import Button from "@/components/Button";
import Display from "@/components/Display";
export default {
  components: {
    Button,
    Display
  },
  methods: {
    clearMemory() {
      console.log("Limpar memória!");
    },
    setOperation(o) {
      console.log(`Operação ${o}`);
    },
    addDigit(d) {
      console.log(`Digito ${d}`);
    }
  }
};
</script>

<style>
.calculator {
  height: 320px;
  width: 235px;
  border-radius: 5px;
  overflow: hidden;
  display: grid;
  grid-template-columns: repeat(4, 25%);
  grid-template-rows: 1fr 48px 48px 48px 48px 48px;
}
</style>