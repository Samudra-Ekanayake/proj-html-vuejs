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
                <div class="row">
                    <div class="col-3 bg-warning">
                        Logo
                    </div>
                    <div class="col-7 bg-success">
                        link
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
}
</style>
