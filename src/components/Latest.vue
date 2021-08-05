<template>
    <div class="slide">

        <p class="slide__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  LATEST ARTICLE
        </p>

        <h1 class="slide__title">
            Check Our Insights
        </h1>

        <p class="slide__paragraph">
           See the face of Mars, anyhow, and that will be a rare experience seems to me that a view of the heavenly bodies through a fine telescope, as well as a tour round the world.
        </p>

        <div class="latest__blog d-flex align-items-center justify-content-between">
            <img src="@/assets/latest.png" alt="">
            <div class="latest__blog-part">
               <h1 class="part__title">
                    What looked like a small 
                    patch of purple grass
                </h1> 

                <p class="part__paragraph">
                    Truly it was a great journey, and in it I met with many, whom to know was to love.
                </p>
            </div>
        </div>
        
        <div class="latest-main d-flex align-items-center justify-content-between" >
                    <div class="latest" v-for="(item,index) in latest" :key='index' >
                    <div class="latest-img">
                        <img class="latest__img" :src="item.img" alt="">
                    
                    </div>
                

                    <h3 class="latest__name">
                        {{ item.title }}
                    </h3>
                </div>
        </div>

        <botton class="latest-btn btn">
            Browse All
        </botton>
    
    </div>
</template>

<script>

export default {
    name:'Latest',

    props: [
       "latest"
    ],
    
   
}
</script>

<style lang="scss"  >

.slide__name{
    max-width: 100% !important;
    margin:0 40% ;
}

.latest{
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
            max-width: 100%;
        }

        &__text{
            font-size: 16px;
            line-height: 32px;
            color: rgba(51, 51, 51, 0.496405);
        }
    }

.latest__blog{
    text-align: start;
    margin: 36px 0;

    &-part{
        max-width: 50%;
        .part__title{
        font-weight: bold;
        font-size: 40px;
        line-height: 48px;
        letter-spacing: -1px;
        color: #333333;

    }

    .part__paragraph{
        font-size: 20px;
        line-height: 32px;
        color: #333333;
    }
    }
    
    
}
     
.latest-btn{
        margin-top: 32px;
    }  

  

@media  screen and (max-width:980px){
 .latest-main{
     display: flex;
     flex-direction: column;
 }

 .latest__img{
     max-width: 100%;
 }

 .latest__blog{
    flex-direction: column;
    img{
        max-width: 100%;
    }
    &-part{
        max-width: 50%;
        .part__title{
        font-size: 28px;

    }

    .part__paragraph{
        font-size: 16px;
    }
    }
    
    
}

}

</style>