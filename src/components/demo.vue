<template>
     <h2 v-bind:style="inDemo">Hello I'm Demo.Vue</h2>
    <template v-if="display">
       
        <h2>GeoSpoc</h2>
        <h2 v-show="showData">Vue JS v-Show </h2>

        <h2 v-for="(name, index) in names" :key="name">{{index}} {{ name}} </h2>

        <h2  v-for="name in fullNames" :key="name.first"> {{name.first}} {{name.last}}</h2>
        <div v-for="emp in employees" :key="emp.empName">
          <h2 class="font-bold" >{{emp.empName}}</h2>
          <h5 v-for="addr in emp.address" :key="addr">{{ addr }}</h5>
        </div>
        <hr class="border border-orange-600">
        <h1 v-for="(data, key, index) in myInfo" :key="data">{{index}} {{key}} {{data}}</h1>
        <h5>H5</h5>

    </template>
  
 

</template>

<script>

  export default {
    name:'App',
    data(){
        return {
            display: true,
            inDemo: {
                fontSize: '30px',
                color: 'white',
                backgroundColor: 'black',
                border: '1px solid gray'
            },
            showData: false,
            names: ['Mayur', 'Aniket', 'Vishal', 'Satya', 'Rajat'],
            fullNames: [
              {first: 'Mayur', last: 'Wakikar'},
              {first: 'Vishal', last: 'Walekar'},
              {first: 'Satya', last: 'Auti'},
            ],
            employees: [
              {
                empName: 'Mayur Wakikar',
                address: ['Pune', 'Parbhani'],
              },
              {
                empName: 'Vishal Walekar',
                address: ['Pune', 'Satara'],
              },
              {
                empName: 'Satya Auti',
                address: ['Pune', 'Rajuri'],
              },
            ],
            myInfo: {
              name: 'Satya',
              address: 'Rajuri',
              company: 'Geospoc'
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
