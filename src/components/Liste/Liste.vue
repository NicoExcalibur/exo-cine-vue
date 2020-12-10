<template>
    <div>
        <ul class="liste mt-5">
            <li v-for="(film, index) in myArr" v-bind:key="index">
                <div class="card">
                    <div class="card-body">
                        Titre : {{ film.titre }}
                        <br>
                        Date : {{ film.date }}
                    </div>
                </div>
            </li>
        </ul>
        <p>{{ txt }}</p>

        <div v-on:click="delFilm" class="btn btn-danger mt-3">
            Supprime le film
        </div>
        <div v-on:click="delTxt" class="btn btn-danger mt-3 ml-2">
            Supprime le txt
        </div>

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
    methods: {
        delFilm: function(){
            this.myArr.pop()
        },
        delTxt: function(){
            this.txt = ""
        }
    },
    props: ['myArr', 'txt']
    

}
</script>

<style scoped src="./Liste.css">


</style>