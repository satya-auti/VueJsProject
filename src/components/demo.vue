<template>
     <h2 v-bind:style="inDemo">Hello I'm Demo.Vue</h2>
    <template v-if="display">
       
        <h2>GeoSpoc</h2>
    </template>
  
 

</template>

<script>

  export default {
    name: 'App',
    data(){
        return {
            display: true,
            inDemo: {
                fontSize: '30px',
                color: 'white',
                backgroundColor: 'black',
                border: '1px solid gray'
            },
        };
    },
  };
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
