<template>
     <h2 v-bind:style="inDemo2">Hello I'm Demo2.Vue</h2>
    <template v-if="display">
       
        <h2 class="font-bold rounded-lg bg-gray-600 text-white">GeoSpoc</h2>
        <!-- <form>
            <div>
                <table>
                    
                </table>
            </div>
        </form>
        <input type="text" name="fullName" id="fullName" placeholder="Full Name"/>
        <input type="email" id="email" name="email" placeholder="Email"/> -->
    </template>
    <!-- <template v-for="name in names" :key="name">
    <h2> {{ name }} </h2>
    <input placeholder="Last Name" />
    <hr/>

    </template>
    <button class="rounded bg-orange-700 p-1 px-3 text-white" @click="shuffle">Shuffle!</button> -->
  <template v-for="name in names" :key="name" >
  <h2 v-if="name === 'pr' || name === 'Satya' ">{{ name }}</h2> 
  
  </template>
  <h2> Addition is {{add(5,3)}} D is {{d}}</h2>
  <button class="rounded px-3 p-1 bg-amber-600 text-white" v-on:mouseover="d=91">Change Value</button>

  <!-- <h2 v-show="count>0" class="rounded-full bg-cyan-700 text-white">{{count}}</h2>
  <button v-on:click="count += 1" class="rounded-xl bg-sky-600 text-white px-3 p-1">Increment</button>
  <button v-on:click="count -= 1" class="rounded-xl bg-red-500 text-white px-3 p-1">Decrement</button> -->
 
 <!-- <h2 v-show="count>0" class="rounded-full bg-cyan-700 text-white">{{count}}</h2>
  <button v-on:click="count += 1" class="rounded-xl bg-sky-600 text-white px-3 p-1">Increment</button>
  <button v-on:click="count -= 1" class="rounded-xl bg-red-500 text-white px-3 p-1">Decrement</button> -->

<h2> {{name}}</h2>
  <button v-on:click="changeName($event),increment(1, $event)" class="rounded-xl bg-sky-600 text-white px-3 p-1">Change Name</button>

<h2 class="rounded-full bg-cyan-700 text-white">{{count}}</h2>
  <button @click="increment(1, $event)" class="rounded-xl bg-sky-600 text-white px-3 p-1">Increment 1</button>
  <button @click="increment(5)" class="rounded-xl bg-red-500 text-white px-3 p-1">Increment 5</button>
  <button @click="decrement(1)" class="rounded-xl bg-sky-600 text-white px-3 p-1">Decrement 1</button>
  <button @click="decrement(5)" class="rounded-xl bg-red-500 text-white px-3 p-1">Decrement 5</button>

</template>

<script>

  export default {
    name:'App',
    data(){
        return {
            display: true,
            inDemo2: {
                fontSize: '30px',
                color: 'red',
                backgroundColor: 'black',
                border: '1px solid gray'
            },
            names: ['Mayur', 'Aniket', 'Vishal', 'Satya', 'Rajat'],
            d: 99,
            count: 0,
            name: 'Satyawan',
        };
    },
    methods: {
        add(a,b) {
           let c = a + b;
            console.log(c);
            return c; 
        },
        changeName(event) {
            this.name = "Satya"
            console.log('Event', event); 
        },
        increment(num) {
            this.count += num
        },
        decrement(num) {
            this.count -= num
        },
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
