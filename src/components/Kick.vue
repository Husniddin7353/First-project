<template>
    <div>
        <div class="kick d-flex align-items-center justify-content-between ">
        <div class="kick__item">
                <h1 class="kick__item-title">
                    Kickstart <br>
                    Your Next <br>
                    Project
                </h1>

                <button class="kick-btn btn">
                    Contact Us
                </button>
            </div>

            <div class="kick__item">
                <p class="kick__item-paragraph">
                    I shall see the face of Mars, anyhow, and that will be a rare experience. It seems to me that a view of the heavenly bodies through a fine telescope, as well as a tour round the world, should form a part of a liberal education.
                </p>


            </div>
            <img src="@/assets/line.png" alt="" class="line">
        </div>

        <div class="email d-flex align-items-center justify-content-between">
            <h3 class="email-title">
                Company Newspaper
            </h3>

            <form action="">
                <input class="email-add" type="email" placeholder="Your Email">
                <input class="email-sub" type="submit" value="Subcripe">
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name:'Kick'
}
</script>

<style lang="scss">
.kick {
background-color: #F07566;
position: relative;
padding: 49px 50px 46px 50px;
margin-top: 10%;
border-radius: 8px;

&__item{
    max-width: 50%;

    &-title{
        font-weight: bold;
        font-size: 56px;
        line-height: 64px;
        letter-spacing: -1px;
        color: #FFFFFF
    }

    &-paragraph{
        font-size: 16px;
        line-height: 32px;
        color: #FFFFFF;
    }
}

&-btn{
    background: #FBD34B;
    border-radius: 6px;
    color: black !important;
    margin-top: 33px;

    &:hover{
        background-color: white !important;
    }
}

.line{
    position: absolute;
    bottom: -2rem;
    left: 40%;
}
}

.email{
    margin: 106px 0;
    .email-title{
        font-weight: bold;
        font-size: 40px;
        line-height: 48px;
        letter-spacing: -1px;
        color:#333333;
    }

    .email-add{
        background: #FFFFFF;
        border: 1px solid #DADADA;
        border-radius: 6px;
        padding: 11px 32px;
        margin-right: 30px;
    }

    .email-sub{
        background: #F07566;
        border-radius: 6px;
        font-weight: bold;
        font-size: 16px;
        line-height: 26px;
        text-align: center;
        letter-spacing: 1px;
        text-transform: uppercase;
        color: #FFFFFF;
        border: none;
        cursor: pointer;
        padding: 11px 32px;
    }
}

@media screen and(max-width:980px) {
    .kick {
        flex-direction: column;
        &__item{
            &-title{
                font-size: 36px;
                line-height: 44px;
            }

            &-paragraph{
                font-size: 14px;
                line-height: 24px;
            }
        }
        .line{
        max-width: 50%;
        }
    }

    .email{
    flex-direction: column;
    .email-title{
        font-size: 40px;
        }
    
    .email-add{
        padding: 6px 16px;
        margin: 6px 0;
    }
    .email-sub{
        background: #F07566;
        border-radius: 6px;
        font-weight: bold;
        font-size: 16px;
        line-height: 26px;
        text-align: center;
        letter-spacing: 1px;
        text-transform: uppercase;
        color: #FFFFFF;
        border: none;
        cursor: pointer;
        padding: 6px 16px;
    }
}
}
</style>