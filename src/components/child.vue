<template>
<inner-child></inner-child>
    <h1>Hello I'm child component of user_registration</h1>
    <h1>User Registration Form </h1>
</template>
<script>
import InnerChild from './innerChild.vue';
    export default {
        name:'App',
        components:{ InnerChild }
        
    };

</script>

<style>

</style>
