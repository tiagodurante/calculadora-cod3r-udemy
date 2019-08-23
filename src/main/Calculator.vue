<template>
  <div class="calculator">
    <Display value="10000" />
    <Button triple label="AC" />
    <Button operation label="/" />
    <Button label="7" />
    <Button label="8" />
    <Button label="9" />
    <Button operation label="x" />
    <Button label="4" />
    <Button label="5" />
    <Button label="6" />
    <Button operation label="-" />
    <Button label="1" />
    <Button label="2" />
    <Button label="3" />
    <Button operation label="+" />
    <Button double label="0" />
    <Button label="." />
    <Button label="=" operation />
  </div>
</template>

<script>
import Button from "@/components/Button";
import Display from "@/components/Display";
export default {
  components: {
    Button,
    Display
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