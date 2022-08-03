<template>
    <p>Reaction Timer : {{ score }} ms</p>
    <h5 class="text-bold fs-3 text-success">{{rank}}</h5>
</template>

<script>
export default {
    name: 'Result-vue',
    props:['score'],
    data() {
        return {
            rank: null
        }
    },
   mounted() {
    if(this.score < 250){
        this.rank = 'You have ninja finger'
    }else if(this.score < 400){
        this.rank = 'You are not bad!'
    }else{
        this.rank = 'You should try better!'
    }
   },
}
</script>

<style>

</style>