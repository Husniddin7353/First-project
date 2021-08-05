<template>
    <div class="header d-flex align-itmes-center justify-content-between">
        
        <img class="back-im" src="@/assets/back2.png" alt="">
        <h1 class="main-logo">CMP</h1>
        <nav class="nav" :class="{'active': BurgerOpen}">
            
            <a href="#" class="nav__link">About</a>
            <a href="#" class="nav__link">Portfolio</a>
            <a href="#" class="nav__link">Service</a>
            <a href="#" class="nav__link">Blog</a>
            <a href="#" class="nav__link">Contact</a>

            <span class="header__close" id="close-burger" @click="BurgerOpen = !BurgerOpen">
            +
            </span>
        </nav>

        <button class="header__btn btn ">
            Contact
        </button>

        

        <button class="btn header__burger" @click="BurgerOpen = !BurgerOpen"  id="burger">
            <svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M24 48C37.2548 48 48 37.2548 48 24C48 10.7452 37.2548 0 24 0C10.7452 0 0 10.7452 0 24C0 37.2548 10.7452 48 24 48Z" fill="#F07566"/>
                <path fill-rule="evenodd" clip-rule="evenodd" d="M13 16C13 15.4477 13.4477 15 14 15H34C34.5523 15 35 15.4477 35 16C35 16.5523 34.5523 17 34 17H14C13.4477 17 13 16.5523 13 16ZM13 24C13 23.4477 13.4477 23 14 23H34C34.5523 23 35 23.4477 35 24C35 24.5523 34.5523 25 34 25H14C13.4477 25 13 24.5523 13 24ZM14 31C13.4477 31 13 31.4477 13 32C13 32.5523 13.4477 33 14 33H34C34.5523 33 35 32.5523 35 32C35 31.4477 34.5523 31 34 31H14Z" fill="white"/>
            </svg>

        </button>

        
    </div>
</template>

<script>
export default {
   name: 'MainHeader',
    data(){
    return{
      BurgerOpen: false,
    }
  },
  watch:{
    BurgerOpen(){
      if (this.BurgerOpen){
        document.body.style.overflow="hidden"
      } else {
        document.body.style.overflow="scroll"
      }
    }
  }

}
</script>

<style lang="scss">
.header{

    .back-im{
        position: absolute;
        right: 0;
        z-index: -1;
        top: 0;
        overflow: hidden;

    }
}
.header{
  .main-logo{
    font-weight: bold;
    font-size: 40px;
    line-height: 48px;
    letter-spacing: -1px;
    color: #333333;

  }
    padding: 16px 0;
    .nav{
        padding-top: 6px;
        img{
            margin-right: 42px;
        }
        &__link{
            margin: 0 24px;
            font-size: 16px;
            line-height: 32px;
            color: #333333;
            text-decoration: none;

            &:hover{
                 color: #F07566;
                 transition: 0.3s all;
            }

        }
    }

    .btn {
        outline:none !important;
        
    }

    &__btn{
        font-weight: bold;
        font-size: 16px;
        line-height: 26px;
        text-align: center;
        letter-spacing: 1px;
        text-transform: uppercase;
        color: #F07566;
        border: 1px solid rgba(240, 117, 102, 0.236809);
        border-radius: 6px;

        &:hover{
    
            background-color:#F07566 ;
            color: white;
            transition: 0.3s all;
        }
    }

    &__burger{
        display: none;
    }

    &__close{
        display: none;
    }
}

@media  screen and (max-width:980px) {
     .header {
       .back-img{
        overflow: hidden;
      }
    .nav{
      display: block;
    }

    .nav{
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      z-index: 22;
      display: flex;
      flex-direction: column;
      background-color: #F07566;
      transition: 0.3s all;
      align-items: center;
      gap: 20px;
      justify-content: center;
      transform: translate(100%);
      .nav__link{
        font-size: 32px;
        margin: 0;
        color: white;

        &:hover{
            color: #F07566;
        }
        


        
      }

      .btn{
        display: block;
      }

      .header__close{
        position: absolute;
        color: white;
        top: 20px;
        right: 20px;
        font-size: 80px;
        font-weight: 600;
        transform: rotate(45deg);
        display: block;
        transition: all 0.2s;
        cursor: pointer;

        &:hover{
          transform: rotate(90deg);
        }
      }

    }

    &__burger{
      display: block;
      cursor: pointer;
      border: none !important;
    }

    &__btn{
      display: none;
    }

    .nav.active{
      transform: translate(0);
    }
  }
    
}

</style>