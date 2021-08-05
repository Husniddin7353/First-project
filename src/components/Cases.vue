<template>
    <div class="cases">
        <p class="cases__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  PARTFOLIO
        </p>

        <h1 class="cases__title">
            Company Cases
        </h1>

        <p class="cases__paragraph">
            Apparently we had reached a great height in the atmosphere, for the sky was a dead black, and the stars had ceased to twinkle the same illusion which lifts the horizon of the sea.
        </p>

        <div class="parts">
            <div class="part" v-for="(item, index) in projects" :key="index">
                <div class="part-img">
                    <img class="part__img" :src="item.img" alt="">
                    <a class="part__link" href="#"> {{ item.id }} </a>
                </div>
                

                <h3 class="part__name">
                    {{ item.title }}
                </h3>

                <p class="part__text">
                    {{ item.text }}
                </p>
            </div>

          

            
        </div>
        <button class="btn cases__btn ">
              BROWSE ALL
          </button>
    </div>
</template>

<script>
export default {
    name:'Cases',

    props: [
       "img", "projects"
    ]
}
</script>

<style lang="scss">

.cases{
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

    &__btn{
        text-align: center;
    }

    .parts{
        display: flex;
        flex-wrap: wrap;
        gap: 5rem;
        
        

        .part{
            border: none;
            

            &-img{
                position: relative;
                img{
                    border-radius: 0 0 0 20px;
                    width: 100%;
                    height: 100%;
                    overflow: hidden;
                }
            }
            &__link{
                position: absolute;
                bottom: 0;
                left: 0;
                background: #4DB282;
                border-radius: 0px 24px 0px 8px;
                padding: 20px 20px 20px 30px;
                font-weight: bold;
                font-size: 40px;
                line-height: 48px;
                text-align: center;
                letter-spacing: -1px;
                color: #FFFFFF;
                text-decoration: none;

                &:hover{
                    background-color: #98e4bf;
                    color: #4DB282;
                    transition: all 0.3s ;
                }

                
            }

            &__name{
                font-weight: bold;
                font-size: 24px;
                line-height: 32px;
                text-align: center;
                color: #333333;
                padding: 8px 0;
            }

            &__text{
                font-size: 16px;
                line-height: 32px;
                text-align: center;
                color: rgba(51, 51, 51, 0.496405);
            }
        }
    }
}

@media  screen and (max-width:980px){
    .parts{
        display: flex !important;
        flex-direction: column;

        .part{
           
            &__link{
                left: 7rem;
            }
        }
    
    }
}

</style>