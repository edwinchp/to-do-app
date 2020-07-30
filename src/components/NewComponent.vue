<template>
    <button v-on:click="counter++">{{msg + " " + counter}}</button>
</template>

<script>
export default {
   data(){
       return{
           msg: "Click me to increment",
           counter: 0
       }
   }
}
</script>

<style lang="stylus" scoped>

</style>