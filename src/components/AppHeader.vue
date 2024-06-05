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

            HeaderSlide: [
                {
                    title: 'Accelerate Your Career',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi maxime nisi tempora. Tempora quisquam optio autem, quod mollitia eius veniam dolore nam, ipsum fuga tenetur quae amet enim itaque porro.',
                    image: 'src/assets/h5-slide-1-background.jpg'
                },

                {
                    title: 'Premium Education',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi maxime nisi tempora. Tempora quisquam optio autem, quod mollitia eius veniam dolore nam, ipsum fuga tenetur quae amet enim itaque porro.',
                    image: 'src/assets/h5-slide-2-background.jpg'
                },

                {
                    title: 'Contemporary Ideas',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi maxime nisi tempora. Tempora quisquam optio autem, quod mollitia eius veniam dolore nam, ipsum fuga tenetur quae amet enim itaque porro.',
                    image: 'src/assets/h5-slide-3-background.jpg'
                },
            ],

            currentSlide: 0,
            interval: null
        }
    },

    methods: {

        nextSlide() {
            this.currentSlide = (this.currentSlide + 1) % this.HeaderSlide.length;
        },
        prevSlide() {
            this.currentSlide = (this.currentSlide - 1 + this.HeaderSlide.length) % this.HeaderSlide.length;
        },
        startCarousel() {
            this.interval = setInterval(this.nextSlide, 3000); // Cambia immagine ogni 3 secondi
        },
        stopCarousel() {
            clearInterval(this.interval);
            this.interval = null;
        }

    },

    mounted() {

        this.startCarousel(); // Avvia il carosello quando il componente è montato
    },

    beforeDestroy() {
        this.stopCarousel(); // Ferma il carosello quando il componente viene distrutto
    }




}


</script>

<template>
    <!-- NAVBAR -->
    <div class="container-fluid st_slideContainer" :style="{ backgroundImage: `url(${HeaderSlide[currentSlide].image})` }">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <div class="row mt-4">
                        <div class="col-3 st_logo">
                            <img src="../assets/logo-light.png" alt="">
                        </div>
                        <div class="col-7 st_links">
                            <ul class="d-flex">
                                <li class="mx-4" v-for="element in navList">
                                    <a href="">{{ element }}</a>
                                </li>
                            </ul>
                        </div>
                        <div class="col-2 st_icons ">
                            <i class="fa-solid fa-magnifying-glass"></i>
                            <i class="fa-solid fa-bag-shopping"></i>
                            <i class="fa-solid fa-bars"></i>
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <div class="container-fluid st_containerMain ">
            <div class="row">
                <div class="col-12">
                    <!-- <h2>{{ HeaderSlide[currentslide].title }}</h2> -->
                    <p></p>

                </div>
            </div>
        </div>
    </div>

    <button @click="nextSlide">Next</button>
    <button @click="prevSlide">Previous</button>


    <AppCard />



</template>

<style scoped>

.st_slideContainer {
    background-color: blanchedalmond;
}
.st_containerMain {
    height: 40rem;
    margin-bottom: 4rem;
    background-size: cover;   
    background-position: center;   
    transition: background-image 1s ease-in-out;

}

.st_logo img {
    margin-left: 4rem;
    height: 2rem;
}

.st_logo {
    display: flex;
    align-items: center;
}

.st_icons {
    display: flex;
    align-items: center;
    justify-content: space-around;
    color: white;
}

.st_links {
    display: flex;
    align-items: center;
    justify-content: center;

}

a {
    text-decoration: none;
    color: white;
}

ul {
    list-style-type: none;
}

.slide {
    display: none;
}

.active {
    display: block;
}
</style>
