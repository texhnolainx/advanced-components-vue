<template>
    <div>
        <h3>New Quote</h3>
        <button @click="counter++">Increase</button>
        <p>{{ counter }}</p>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
              counter: 0  
            };
        },
        destroyed() {
            console.log(`New quote is killed!`);
        },
        deactivated() {
            console.log(`Fuck you, deactivating me...`);
        },
        activated() {
            console.log(`Oh nice, you're back!`);
        }
    }
</script>

<style>
</style>