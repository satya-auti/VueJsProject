<template>
     <h2 v-bind:style="inDemo2">Hello I'm Demo2.Vue</h2>
    <template v-if="display">
       
        <h2>GeoSpoc</h2>
        <form>
            <div>
                <table>
                    
                </table>
            </div>
        </form>
        <input type="text" name="fullName" id="fullName" placeholder="Full Name"/>
        <input type="email" id="email" name="email" placeholder="Email"/>
    </template>
  
 

</template>

<script>

  export default {
    name: 'App',
    data(){
        return {
            display: true,
            inDemo2: {
                fontSize: '30px',
                color: 'red',
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
