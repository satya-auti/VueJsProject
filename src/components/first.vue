<template>
  
    <h2 v-bind:style="inFirst">Hello I'm first.Vue</h2>
   <h2 v-bind:style="objectStyle">Hello Vue from 1st Comp.</h2>
   <h2 v-if="num===5">The Number is Five.</h2>
   <h2 v-else-if="num<0">The Number Negative.</h2>
   <h2 v-if="num>0">The Number is Positve.</h2>
   <h2 v-else>Not a Number.</h2>
</template>

<script>


  export default {
    name: 'App',
    data(){
        return {
            num: 5,
            objectStyle: {
                fontSize: '30px',
                color: 'red',
                fontStyle: 'italic'
            },
            inFirst: {
                fontSize: '30px',
                color: 'red',
                backgroundColor: 'yellow',
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
