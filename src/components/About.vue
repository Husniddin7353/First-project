<template>
    

    <div class="about d-flex align-items-center justify-content-between">
        
        <img class="image" src="@/assets/gr2.png" alt="">
        <section class="inform">
            <p class="inform__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  ABOUT
            </p>

            <h1 class="inform__title">
                WE BUILD <br> PRO BUSSUNISS
            </h1>

            <h3 class="inform__title-tail">
                Excited to work with customers
            </h3>

            <p class="inform__paragraph">
                <svg width="24" height="22" viewBox="0 0 24 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M22 11C22 10.421 21.942 9.857 21.856 9.303L19.99 11.205C19.879 16.072 15.894 20 11 20C6.038 20 2 15.962 2 11C2 6.038 6.038 2 11 2C12.8 2 14.474 2.537 15.882 3.45L17.304 1.993C15.518 0.741 13.347 0 11 0C4.925 0 0 4.925 0 11C0 17.075 4.925 22 11 22C17.075 22 22 17.075 22 11ZM11.5 10.806L20.904 1.167L24 4.263L11.5 17L4.562 10.29L7.657 7.192L11.5 10.806Z" fill="#4DB282"/>
                </svg>

                The sky was cloudless and of a deep 
            </p>

            <p class="inform__paragraph">
                <svg width="24" height="22" viewBox="0 0 24 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M22 11C22 10.421 21.942 9.857 21.856 9.303L19.99 11.205C19.879 16.072 15.894 20 11 20C6.038 20 2 15.962 2 11C2 6.038 6.038 2 11 2C12.8 2 14.474 2.537 15.882 3.45L17.304 1.993C15.518 0.741 13.347 0 11 0C4.925 0 0 4.925 0 11C0 17.075 4.925 22 11 22C17.075 22 22 17.075 22 11ZM11.5 10.806L20.904 1.167L24 4.263L11.5 17L4.562 10.29L7.657 7.192L11.5 10.806Z" fill="#4DB282"/>
                </svg>

                The sky was cloudless and of a deep 
            </p>

            <p class="inform__paragraph">
                <svg width="24" height="22" viewBox="0 0 24 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M22 11C22 10.421 21.942 9.857 21.856 9.303L19.99 11.205C19.879 16.072 15.894 20 11 20C6.038 20 2 15.962 2 11C2 6.038 6.038 2 11 2C12.8 2 14.474 2.537 15.882 3.45L17.304 1.993C15.518 0.741 13.347 0 11 0C4.925 0 0 4.925 0 11C0 17.075 4.925 22 11 22C17.075 22 22 17.075 22 11ZM11.5 10.806L20.904 1.167L24 4.263L11.5 17L4.562 10.29L7.657 7.192L11.5 10.806Z" fill="#4DB282"/>
                </svg>

                The sky was cloudless and of a deep 
            </p>

            <button class="inform__btn btn">LEARN MORE</button>
        </section>

        
    </div>
</template>

<script>
export default {
  name:'About'  
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
            font-weight: bold;
            font-size: 24px;
            line-height: 32px;
            color: #333333;
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