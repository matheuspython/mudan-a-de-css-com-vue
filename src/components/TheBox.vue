<template>
  <div 
    v-on:click="changeColor" 
    :style="{ background: cor }"
  >
    <h2>click for change my color</h2>
  </div>
</template>

<script>
export default {
  name: "TheBox",
  props: {
    color: String,
    secondaryColor: String,
  },
  data() {
    return {
      cor: this.color,
      colorContext: this.color,
      secondaryColorContext: this.secondaryColor,
      changeColor() {
        this.cor == this.colorContext
          ? (this.cor = this.secondaryColorContext)
          : (this.cor = this.colorContext);
      },
    };
  },
};
</script>

<style scoped>
div {
  width: 300px;
  height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  max-width: 100%;
  padding: 25px;
  border-radius: 12px;
  font-size: 16px;
}
</style>
