<template>
    <div class="container mt-5">
        <liste v-bind:myArr="myArr" :txt="txt"></liste>
        <liste v-bind:myArr="myArr" :txt="txt"></liste>
    </div>
</template>

<script>

import Liste from './Liste/Liste.vue'

export default {
    name: 'Contenu',
    data(){
        return {
            myArr : [
                {titre: 'Inception', date: 2010},
                {titre: 'Avatar', date: 2009},
                {titre: 'Seven', date: 1995}
            ],
        txt: 'Hello !'
        }
    },
    components: {
        'liste': Liste
    }
}

</script>

<style>
</style>