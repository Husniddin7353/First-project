<template>
    

    <div class="test d-flex align-items-center justify-content-between">
        
        <img class="image" src="@/assets/gr2.png" alt="">
        <section class="inform">
            <p class="inform__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  TESTIMONIELS
            </p>

            <h1 class="inform__title">
               Reviews
            </h1>

            <div class="comment">
            <p class="comment__paragraph">
                "The sky was cloudless and of a deep dark blue the spectacle before us was indeed sublime sky was cloudless and of a deep dark."
            </p>

            <h3 class="comment__title-tail">
                Jaroslav Brabec
            </h3>

            <p class="comment__text">
                Microsoft
            </p>
            </div>

            <button class="comment__btn btn">
                <svg width="12" height="20" viewBox="0 0 12 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M0.325817 9.2196L9.41557 0.31951C9.62581 0.113495 9.90645 0 10.2057 0C10.5049 0 10.7856 0.113495 10.9958 0.31951L11.6652 0.974789C12.1008 1.40178 12.1008 2.09576 11.6652 2.52209L4.03233 9.99585L11.6737 17.4779C11.8839 17.6839 12 17.9586 12 18.2514C12 18.5446 11.8839 18.8192 11.6737 19.0254L11.0043 19.6805C10.7939 19.8865 10.5134 20 10.2142 20C9.91492 20 9.63428 19.8865 9.42404 19.6805L0.325817 10.7723C0.115084 10.5656 -0.00066185 10.2897 2.86102e-06 9.99634C-0.00066185 9.70187 0.115084 9.4261 0.325817 9.2196Z" fill="white"/>
                </svg>
            </button>
            <button class="comment__btn btn">
                <svg width="12" height="20" viewBox="0 0 12 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M11.6742 9.2196L2.58443 0.31951C2.37419 0.113495 2.09355 0 1.7943 0C1.49506 0 1.21441 0.113495 1.00418 0.31951L0.334782 0.974789C-0.1008 1.40178 -0.1008 2.09576 0.334782 2.52209L7.96767 9.99585L0.326313 17.4779C0.116078 17.6839 0 17.9586 0 18.2514C0 18.5446 0.116078 18.8192 0.326313 19.0254L0.99571 19.6805C1.20611 19.8865 1.48659 20 1.78583 20C2.08508 20 2.36572 19.8865 2.57596 19.6805L11.6742 10.7723C11.8849 10.5656 12.0007 10.2897 12 9.99634C12.0007 9.70187 11.8849 9.4261 11.6742 9.2196Z" fill="white"/>
                </svg>

            </button>
        </section>

        
    </div>
</template>

<script>
export default {
  name:'Test'  
}
</script>

<style lang="scss">

.inform{
    width: 50%;
    &__name{
        font-weight: bold;
        font-size: 16px;
        line-height: 32px;
        letter-spacing: 1px;
        color: #F07566;

        svg{
            margin-right: 6px;
        }
    }
    &__title{
        font-weight: bold;
        font-size: 56px;
        line-height: 64px;
        letter-spacing: -1px;
        color: #333333;

        
    }
    .comment{
        max-width: 470px;
        background: #FFFFFF;
        box-shadow: 0px 24px 48px rgba(0, 17, 86, 0.0799083);
        border-radius: 8px;
        padding: 16px 32px;

        &__title-tail{
            font-weight: bold;
            font-size: 24px;
            line-height: 32px;
            color: #333333;
        }

    &__paragraph{
      
        font-size: 16px;
        line-height: 32px;
        color: rgba(51, 51, 51, 0.496405);
    }

    &__text{
        font-size: 14px;
        line-height: 24px;
        color: rgba(51, 51, 51, 0.496405);
    }
    }
    .comment__btn{
        background: #F07566;
        border-radius: 50%;
        margin: 12px 4px;
    }
}

@media  screen and (max-width:980px){
    .test{
        display: flex;
        flex-direction: column;

        .image{
            max-width: 80%;
        }
        .comment{
            max-width: 230px;
        }
        .inform__title{
            font-size: 32px;
        }
        .comment__paragraph{
            font-size: 16px;
            line-height: 18px;
        }
    }
}

</style>