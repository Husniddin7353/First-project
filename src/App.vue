<template>
  <div>
      <div class="header container">
        <MainHeader/>
      </div>

      <div class="container">
        <Company/>
        <About/>
        <Blog/>
        <Feature/>
        <Cases :projects="projects" :img="projects.img" :title="projects.title" :text="projects.text" :id="projects.id"/>
        <Partners :partners="partners" :img="partners.img"/>
        <Service/>
      </div>
        <Team :slider="slider"/> 

      <div class="container">
        <Test/>
        <Kick/>
        <Latest :latest="latest"/>
      </div>

      <Footer/>
  </div>
</template>

<script>

import MainHeader from '@/components/MainHeader.vue'
import Company from '@/components/Company.vue'
import About from '@/components/About.vue'
import Blog from '@/components/Blog.vue'
import Feature from '@/components/Feature.vue'
import Cases from '@/components/Cases.vue'
import Partners from '@/components/Partners.vue'
import Service from '@/components/Service.vue'
import Team from '@/components/Team.vue'
import Test from '@/components/Test.vue'
import Kick from '@/components/Kick.vue'
import Latest from '@/components/Latest.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: "App",
  components: {
    MainHeader,
    Company,
    About,
    Blog,
    Feature,
    Cases,
    Partners,
    Service,
    Team,
    Test,
    Kick,
    Latest,
    Footer
  },

  data(){
    return{
      projects:[
        {
          id:"01",
          img: 'https://picsum.photos/570/400',
          title: 'Face of Mars',
          text: 'Will be a rare experience'
        },

        {
          id:'02',
          img: 'https://picsum.photos/569/400',
          title: 'Heavenly Bodies',
          text: 'Tour round the world should form '
        },

        {
          id:'03',
          img: 'https://picsum.photos/568/400',
          title: 'Liberal Education',
          text: 'Truly it was a great journey'
        },

        {
          id:'04',
          img: 'https://picsum.photos/567/400',
          title: 'Though the Gravity',
          text: 'Daily classes he no longer collapsed'
        }
      ],

      partners:[
        { img: require('@/assets/pr1.png') },
        { img: require('@/assets/pr2.png') },
        { img: require('@/assets/pr3.png') },
        { img: require('@/assets/pr4.png') },
        { img: require('@/assets/pr5.png') },
        { img: require('@/assets/pr6.png') },

      ],

      slider:[
          {
          img: 'https://picsum.photos/341/370',
          title: 'Ingo Schimpff',
          text: 'Manager '
        }, 

        {
          img: 'https://picsum.photos/342/370',
          title: 'Gauthier Drewitt',
          text: 'Director '
        }, 
        {
          img: 'https://picsum.photos/340/370',
          title: 'Gauthier Drewitt',
          text: 'Director '
        },
        {
          img: 'https://picsum.photos/341/370',
          title: 'Gauthier Drewitt',
          text: 'Director '
        }, 

        {
          img: 'https://picsum.photos/340/370',
          title: 'Winny Rearie',
          text: 'Manager'
        }
      ],

      latest:[
          
        {
          img: 'https://picsum.photos/340/240',
          title: 'Above five feet square, was moving across',
          
        },
        {
          img: 'https://picsum.photos/341/240',
          title: 'Enough he perceived that it was not grass',
        
        }, 

        {
          img: 'https://picsum.photos/342/240',
          title: 'There were no blades, but only purple roots',
         
        }
      ]
    }
  }
};
</script>



<style lang="scss">
body{
  font-family: sans-serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
a{
  text-decoration: none;
}

img{
  pointer-events: none;
}
.btn:focus {
  outline:none !important;
  }

  .btn{
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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container{
  max-width: 1280px;
  margin: 0 auto; 
}

</style>
