<template>
    <div>
        <p id="box"> </p>
    </div>
</template>

<script>
    export default {

        mounted(){
            let box = document.getElementById(`box`);
            box[`innerHTML`] += `<h2>${this[`num_friends`]} </h2>`;
            box[`innerHTML`] += `<p>user logged is ${this[`logged_in`]}</p>`;
            for(let i =0;i<this[`tweets`].length;i++){
            box[`innerHTML`] += `<p>tweet is ${this[`tweets`][i]}</p>`;
            }
        },
        data() {
            return {
                tweets: [`be humble`,`be positive`,`be honest`],
                num_friends: 100,
                logged_in: true
            }
        }
    }
</script>

<style scoped>

</style>