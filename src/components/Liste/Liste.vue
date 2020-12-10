<template>
    <div>
        <ul class="liste">
            <li v-for="(film, index) in films" v-bind:key="index">{{ film }}</li>
        </ul>
        <p>{{ prenom }}</p>
    </div>
</template>

<script>
export default {
    name: 'Liste',
    data(){
        return{
            films: ['Inception', 'Avatar', 'Seven']
        }
    },
    props: {
        prenom: {
            type : String,
            required: true
        }
    }

}
</script>

<style scoped src="./Liste.css">


</style>