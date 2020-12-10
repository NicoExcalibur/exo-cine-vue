<template>
    <div class="container">
        <p>{{ txt }}</p>
        <liste v-bind:prenom="prenom"></liste>
    </div>
</template>

<script>

import Liste from './Liste/Liste.vue'

export default {
    name: 'Contenu',
    data(){
        return {
            txt: 'oskour',
            prenom: 'Nico'
        }
    },
    components: {
        'liste': Liste
    }
}

</script>

<style>
</style>