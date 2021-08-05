<template>
    <div class="slide">
        <div class="slide-item d-flex align-items-center justify-content-between">
            <img src="@/assets/Rectangle.png" alt="" class="slide-item__back">
            <img src="@/assets/case1.png" alt="" class="case">

            <div class="slide-inform">
                <h1 class="slide-inform__title">
                    Strategy, technology
                    and design
                </h1>
                <p class="slide-inform__text">
                    Apparently we had reached a great height in the atmosphere, for the sky was a dead black.
                </p>
            </div>
        </div>
        <p class="slide__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  Team
        </p>

        <h1 class="slide__title">
            Strong Members
        </h1>

        <p class="slide__paragraph">
           Formed a great hindrance to my speed, I resolved, contrary to my first intention, to make the being of a gigantic stature that is to say, about eight feet in height.   
        </p>
        <VueSlickCarousel  v-bind="settings" >
                <div class="slider" v-for="(item,index) in slider" :key='index'>
                    <div class="slider-img">
                        <img class="slider__img" :src="item.img" alt="">
                    
                    </div>
                

                    <h3 class="slider__name">
                        {{ item.title }}
                    </h3>

                    <p class="slider__text">
                        {{ item.text }}
                    </p>
                </div>
        </VueSlickCarousel> 
    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    name:'Team',
    components:{
        VueSlickCarousel
    },
    props: [
       "slider"
    ],
    data () {
        return {
            settings: {
                arrows: false,
                dots: true,
                slidesToShow: 3,
                dotsClass: "slick-dots custom-dot-class",

                 responsive: [
                {
                    breakpoint: 980,
                    settings: {
                        slidesToShow: 2
                    }
                },
                {
                    breakpoint: 600,
                    settings: {
                        slidesToShow: 1,
                    }
                }]
            },
        }
    }
   
}
</script>

<style lang="scss"  >


.slide-item{
    text-align: start;
       &__back{
           position: absolute;
           left: 0;
           z-index: -1;
           overflow: hidden !important;
           max-width: 100%;
       }
       .slide-inform{
           max-width: 50%;
           &__title{
               font-weight: bold;
                font-size: 56px;
                line-height: 64px;
                letter-spacing: -1px;
                color: #FFFFFF;
           }

           &__text{
               font-size: 20px;
                line-height: 32px;
                color: #FFFFFF;
           }
       }
   }
.slide{
    margin: 150px 0;
   text-align: center;

   
    &__name{
        font-weight: bold;
        font-size: 16px;
        line-height: 32px;
        letter-spacing: 1px;
        color: #F07566;
        max-width: 110px;
        margin: 0 auto;

        svg{
            margin-right: 6px;
        }
    }

    &__title{
        font-weight: bold;
        font-size: 56px;
        line-height: 64px;
        text-align: center;
        letter-spacing: -1px;
        color: #333333;
    }

    &__paragraph{
        font-size: 16px;
        line-height: 32px;
        margin: 28px auto 61px auto;
        text-align: center;
        color: rgba(51, 51, 51, 0.496405);
        max-width: 770px;

    }


    .slider{
        display: flex;
        
        
    }
}

.slider{
        border: 1px solid #E6EDF5;
        border-radius: 8px;
        max-width: 370px;
        text-align: start;
        padding: 16px;
        &:hover{
            box-shadow: 0px 24px 48px rgba(0, 17, 86, 0.0799083);
        }   
        &-img{
            img{
                border-radius: 8px 8px 50px 8px;
                transition: all 0.3s;

            }
        }
        
        &__name{
            font-weight: bold;
            font-size: 24px;
            line-height: 32px;
            color: #333333;
             padding: 8px 0;
        }

        &__text{
            font-size: 16px;
            line-height: 32px;
            color: rgba(51, 51, 51, 0.496405);
        }
    }
     
    .slick-dots {
    padding-left: 5px;
    margin: -32px 0;

    .slick-active{
      display: inline-block;
      list-style: none;
        &:first-child {
        margin-left: 0;
      }

      button{
          background-color: #F07566;
          border-radius: 50%;
      }
    }
  
}

  

@media  screen and (max-width:980px){
 

    .case{
        max-width: 80%;
    } 
    
    
    .slide-item{
    flex-direction: column;
    background-color: #F07566;
    max-width: 110%;
      &__back{
          overflow: hidden;
          max-width: 100%;
      }

      &__img{
          max-width: 80%;
          height: 100%;
      }
   }
}

</style>