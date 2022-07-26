<template>
  <header :class="color" v-on:click="changeColor()">
    {{ title }}
  </header>
</template>

<script>
  export default{
    name: 'TheuHeader',
    props: {
      title: String
    },
    data(){
      return{
        color: 'blue',
        changeColor: () => {
          if(this.color === 'blue'){ return this.color = 'black'  }

          this.color = 'blue'
        }
      }
    }

  }
</script>

<style scoped>
  header{
    width: 100%;
    height: 75px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    font-size: 20px;
    text-transform: uppercase;
  }
  .black{
    background-color: rgb(34, 34, 34);
  }
  .blue{
    background-color: rgb(21, 77, 189);
  }
</style>