<script>
export default {
    name: 'AppCard',

    data() {
        return {

            cards: [
                {
                    title: 'Languages',
                    img: 'src/assets/h5-custom-icon-1.png'
                },
                {
                    title: 'Software',
                    img: 'src/assets/h5-custom-icon-2.png'
                },
                {
                    title: 'Buisness',
                    img: 'src/assets/h5-custom-icon-3.png'
                },
                {
                    title: 'Chemistry',
                    img: 'src/assets/h5-custom-icon-4.png'
                },
                {
                    title: 'Science',
                    img: 'src/assets/h5-custom-icon-5.png'
                },
                {
                    title: 'DIY&Craft',
                    img: 'src/assets/h5-custom-icon-6.png'
                },

            ]

        }
    },

    methods: {


    },

    mounted() {

    },

}

</script>

<template>

    <div class="container-fluid">
        <div class="row d-flex justify-content-center">
            <div v-for="element in cards" class="col-2 st_square d-flex flex-column align-items-center pt-4">
                <div class="st_card">
                    <img :src="element.img" alt="">
                </div>
                <div>
                    <h3>{{ element.title }}</h3>
                </div>
            </div>
        </div>
    </div>



</template>

<style scoped>
.st_square {
    margin: 1rem;
    height: 12rem;
    width: 12rem;
    background-color: bisque;
}

.st_card {
    margin-bottom: 2rem;
}
</style>