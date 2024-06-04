<script>

import AppCard from './AppCard.vue'


export default {

    components: {
        AppCard
    },


    data() {
        return {
            navList: [
                'HOME', 'COURSES', 'INSTRUCTORS', 'EVENTS', 'PAGES', 'ELEMENTS',
            ],




        }
    },

    methods: {


    },

    mounted() {

    },

}


</script>

<template>
    <!-- NAVBAR -->
    <div class="container-fluid">
        <div class="row">
            <div class="col-12 bg-info">
                <div class="row mt-4">
                    <div class="col-3 bg-warning st_logo">
                        <img src="../assets/logo-light.png" alt="">
                    </div>
                    <div class="col-7 bg-success d-flex justify-content-around">
                        <ul class="d-flex">
                            <li class="mx-4" v-for="element in navList">
                                <a href="">{{ element }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2 bg-primary">
                        icons
                    </div>
                </div>

            </div>
        </div>
    </div>

    <div class="container-fluid st_containerMain">
        <div class="row">
            <div class="col-12">

            </div>
        </div>
    </div>

    <AppCard />

</template>

<style scoped>
.st_containerMain {
    height: 40rem;
    background-color: brown;
    margin-bottom: 4rem;

}

.st_logo img {
    margin-left: 4rem;
    height: 2rem;
}
</style>
