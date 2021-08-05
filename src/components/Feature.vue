<template>
    

    <div class="about d-flex align-items-center justify-content-between">
        
        <section class="inform">
            <p class="inform__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  FEATURES
            </p>

            <h1 class="inform__title">
                Smart Complex 
                Solutions
            </h1>

            <p class="inform__paragraph">
                <svg width="24" height="22" viewBox="0 0 24 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M22 11C22 10.421 21.942 9.857 21.856 9.303L19.99 11.205C19.879 16.072 15.894 20 11 20C6.038 20 2 15.962 2 11C2 6.038 6.038 2 11 2C12.8 2 14.474 2.537 15.882 3.45L17.304 1.993C15.518 0.741 13.347 0 11 0C4.925 0 0 4.925 0 11C0 17.075 4.925 22 11 22C17.075 22 22 17.075 22 11ZM11.5 10.806L20.904 1.167L24 4.263L11.5 17L4.562 10.29L7.657 7.192L11.5 10.806Z" fill="#4DB282"/>
                </svg>

                Stars had ceased to twinkle the same illusion which lifts the horizon of the sea to the level of the spectator on a hillside, the sable cloud beneath was dished out.
            </p>


            <div class="inform__title-tail align-items-center">
             <svg width="24" height="23" viewBox="0 0 24 23" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M8.332 7.62569L12 0L15.668 7.6267L24 8.78546L17.936 14.6569L19.416 22.999L12 19.0028L4.584 23L6.064 14.6579L0 8.78546L8.332 7.62569ZM14.335 9.47468L12 4.62096L9.665 9.47468L4.36 10.2133L8.221 13.9515L7.279 19.2617L12 16.7175L16.721 19.2607L15.779 13.9505L19.64 10.2123L14.335 9.47468Z" fill="#4DB282"/>
            </svg>
                Modern Technology

                <p class="inform__title-tail_text">
                    The sky was cloudless and of a deep dark blue the spectacle before us was indeed sublime.
                </p>
            </div>

        </section>

        
        <img class="image" src="@/assets/gr2.png" alt="">

        
    </div>
</template>

<script>
export default {
  name:'Feature'  
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

        &-tail{
            max-width: 470px;
            font-weight: bold;
            font-size: 24px;
            line-height: 32px;
            color: #333333;
            box-shadow: 0px 24px 48px rgba(0, 17, 86, 0.0799083);
            border-radius: 8px;

            &_text{
                font-size: 14px;
                line-height: 24px;
                color: rgba(51, 51, 51, 0.496405);
                margin: 8px 0;
            }
        }
    }

    &__paragraph{
        svg{
            margin-right: 6px;
        }
        font-size: 20px;
        line-height: 32px;
        color: #333333;
        margin: 35px 0;
        max-width: 470px;
    }

   
}
@media  screen and (max-width:980px){
    .about{
        display: flex;
        flex-direction: column;

        .image{
            max-width: 80%;
        }

        .inform__title{
            font-size: 32px;
        }

        .inform__paragraph{
            font-size: 16px;
        }
    }
}
</style>