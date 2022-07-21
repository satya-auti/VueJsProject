<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
 
  <!-- <div> 
    <h1> Hello {{name}} {{work("Auti")}} </h1>
    <h1 v-html="channel"></h1>
    <h2 class="hover:text-red-600 text-orange-600" v-html="hack"></h2>
  </div>
  <h1 class="text-3xl hover:text-zinc-400 text-amber-600 bg-slate-600 font-bold underline">
    Welcome to the GeoSpoc world!
  </h1>
  <h2 v-bind:id="headingId">Heading</h2>
  <button class="rounded bg-orange-600 px-5 p-1" v-bind:disabled="isDisabled">OK</button>
  <h2 class="underline">Underline Text</h2>
  <h2 v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'"> Satya is Promoted</h2>
  <h2 v-bind:class="isSoldOut ? 'old':'latest' "> Soldout ? Movie</h2>
  <h2 v-bind:class="['latest', 'promoted']">New updated things</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'old':'latest']">Array condition things</h2>
   <h2 v-bind:class="{
    promoted: isPromoted,
    latest: !isSoldOut,
    'old': isSoldOut
   }">Object condition things</h2>
   <h3 v-bind:style="{
    color:highlightColor,
    fontSize: size + 'px',
    padding: '20px'
   }">Inline Style</h3>

   <h2 v-bind:style="headerStyleObject"> Style Objects</h2>

   <div v-bind:style="[baseStyleObject,successStyleObject]">Welcome to Vue JS World!!!</div>
   <div v-bind:style="[baseStyleObject,dangerStyleObject]">Welcome to Danger World!!!</div> -->
   <!-- <div v-bind:style=""> </div> -->
    <h2 v-bind:style="inApp">Hello I'm App.Vue</h2>
   <h2 v-if="num===9">The Number is Nine.</h2>
   <h2 v-else>The Number is not Match.</h2>
   <h2></h2>
   <user_registration></user_registration>
   <first></first>
   <demo2></demo2>
    <demo></demo>
    
</template>

<script>
  import first from './components/first.vue'
  import demo from './components/demo.vue'
  import demo2 from './components/demo2.vue'
  import user_registration from './components/user_registration.vue'


  export default {
    name:'App',
    components:{
    first,
    demo,
    demo2,
    user_registration,
   
},

    data (){
      return {
        num: 9,
        inApp: {
          fontSize: '30px',
          color: 'blue',
          backgroundColor: 'skyblue',
          border: '1px solid gray'
        },
      }
      // return {
      //   greet : "Hello",
      //   name: "Satya ",
      //   channel : "<b>GeoSpoc<b>",
      //   work : function (a) {
      //     return a;
      //   },
      //   hack : `<a href="#" onclick="alert('You have been Hacked!!!')"> ! Win Prize ! <a/>`,
      //   headingId:"Heading",
      //   isDisabled: true,
      //   status: "success",
      //   isPromoted: true,
      //   isSoldOut: true,
      //   highlightColor: 'orange',
      //   size: 80,
      //   headerStyleObject: {
      //     color: "gray",
      //     fontSize: '20px',
      //     padding: '10px',
      //     fontStyle: 'italic'
      //   },
      //   baseStyleObject: {
      //     // color: "blue",
      //     // fontSize: '25px',
      //     // padding: '15px',
      //     backgroundColor: 'gray',
      //     fontStyle: 'italic'
      //   },
      //   successStyleObject: {
      //     color: "green",
      //     fontSize: '35px',
      //     padding: '20px',
      //     border: '2px solid red'
      //     // fontStyle: 'italic'
      //   },
      //   dangerStyleObject: {
      //     color: "darkred",
      //     fontSize: '35px',
      //     padding: '20px',
      //     border: '2px solid blue'
      //     // fontStyle: 'italic'
      //   },
      // };
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
/* h1 {
  color: chocolate;
  background-color: rgb(253, 241, 241);
} */
.underline{
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.latest {
  color: rgb(11, 34, 170);
  font: bold;
}
.old {
  color: red;
}
</style>
