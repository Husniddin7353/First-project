<template>
    <div class=" company d-flex align-items-center justify-content-between">

        <section class="inform">
            <p class="inform__name d-flex align-items-center"> <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F07566"/>
                </svg>  COMPANY
            </p>

            <div class="logo">
                <img src="@/assets/Company.png" alt=""> <br>
                <img src="@/assets/Bitmap.png" alt="">
            </div>

            <p class="inform__paragraph">
                The sky was cloudless and of a deep dark blue the spectacle before us was indeed sublime.
            </p>

            <button class="inform__btn btn">EXPLORE</button>
        </section>
        <img class="image" src="@/assets/gr1.png" alt="">
        
    </div>
</template>

<script>
export default {
  name:'Company'  
}
</script>

<style lang="scss">
.inform{
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

    &__paragraph{
        font-size: 20px;
        line-height: 32px;
        color: #333333;
        margin: 35px 0;
        max-width: 470px;
    }

   
}
@media  screen and (max-width:980px){
    .company{
        display: flex;
        flex-direction: column-reverse;
        position: relative;

        .image{
            max-width: 80%;
        }
        .logo{
            img{
                max-width: 90%;
            }
        }
        .inform__paragraph{
            font-size: 16px;
        }

     
    }
}
</style>