<template>
  <main>
  <h1 v-on:click="changeDisplay" class="title">click on a box or in this title</h1>
    <div class="container" :style="{ flexDirection: atualDisplay }">
      <TheBox color="red" secondaryColor="blue"/>
      <TheBox color="#00ffff16" secondaryColor="#0077ff"/>
      <TheBox color="#eb0f67" secondaryColor="#6cfe4f"/>
      <TheBox color="#754ffe" secondaryColor="#fe4f7b"/>
      <TheBox color="#e39632" secondaryColor="#0f8b5e"/>
      <TheBox color="#8623cc" secondaryColor="#d3b5e8"/>
      <TheBox color="#639ea3" secondaryColor="#f4f72a"/>
      <TheBox color="#c41c43" secondaryColor="#4725ee"/>
    </div>
  </main>
</template>

<script>
import TheBox from './TheBox.vue';
  export default {
    name: "TheMain",
    components: { TheBox },
    data(){
      return {
        atualDisplay: 'row',
        changeDisplay(){
          this.atualDisplay == 'row' ? this.atualDisplay =  'column' : this.atualDisplay = 'row'
        }
      }
    }
}
</script>

<style scoped>
main{
  width: 100%;
}
  .title{
    text-align: center;
    margin: 15px;
    font-size: 50px;
  }
  .container{
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    justify-content: center;
    align-items: center;
    width: 100%;
    max-width: 1280px;
    margin: 0 auto;
  }
</style>