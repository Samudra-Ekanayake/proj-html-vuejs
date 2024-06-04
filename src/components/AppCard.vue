
  <script>
  export default {
    name: 'AppCard',

    data() {
        return {

            cards: [
                { title: 'Languages',
                    img: '../assets/h5-custom-icon-1.png'
                },
                { title: 'Software',
                    img: '../assets/h5-custom-icon-2.png'
                },
                { title: 'Buisness',
                    img: '../assets/h5-custom-icon-3.png'
                },
                { title: 'Chemistry',
                    img: '../assets/h5-custom-icon-4.png'
                },
                { title: 'Science',
                    img: '../assets/h5-custom-icon-5.png'
                },
                { title: 'DIY&Craft',
                    : '../assets/h5-custom-icon-6.png'
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
        <div class="row">
            <div v-for="element in cards" class="col-2 st_square" 
            :style="{backgroundimage:element.img}">
                <div>
                    {{ element.title }}
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
  }
  
 

  </style>